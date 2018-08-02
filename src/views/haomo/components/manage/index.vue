<template>
  <el-container>
      <el-header v-bind:style="{ marginTop: '30px' }" >角色管理</el-header>
<el-container>
    <el-aside width="300px">
        <el-form>
  <el-form-item >
    <el-input placeholder="请输入角色名进行查询"></el-input>
  </el-form-item>
        </el-form>
<el-row >
  <el-col :span="12">
    <el-menu>
       <el-submenu>
        <template slot="title">
          <span>导航一</span>
        </template>
      </el-submenu>
       <el-submenu>
        <template slot="title">
          <span>导航二</span>
        </template>
      </el-submenu>
    </el-menu>
  </el-col>
</el-row>
</el-aside>
   <el-main>
       <el-tabs>
  <el-tab-pane label="菜单权限">
      <el-tree
  :props="props"
  :load="loadNode"
  lazy
  show-checkbox
  @check-change="handleCheckChange">
</el-tree>
  </el-tab-pane>
  <el-tab-pane label="数据权限">
<div v-bind:style="{margin:'10px'}"><el-radio v-model="radio" label="1">无</el-radio></div>
<div v-bind:style="{margin:'10px'}"><el-radio v-model="radio" label="2">本人及下属</el-radio></div>
<div v-bind:style="{margin:'10px'}"><el-radio v-model="radio" label="3">本部门</el-radio></div>
<div v-bind:style="{margin:'10px'}"><el-radio v-model="radio" label="4">本分部</el-radio></div>
<div v-bind:style="{margin:'10px'}"><el-radio v-model="radio" label="5">全部</el-radio></div>
  <div v-bind:style="{margin:'10px'}"> <el-button type="primary" plain>保存</el-button></div>
  </el-tab-pane>
  <el-tab-pane label="文档权限">
 <div v-bind:style="{margin:'10px'}"><el-radio v-model="radio1" label="1">管理</el-radio></div>
  <div v-bind:style="{margin:'10px'}"><el-radio v-model="radio2" label="2">查看</el-radio></div>
    <div v-bind:style="{margin:'10px'}"><el-button type="primary" plain>保存</el-button></div>
  </el-tab-pane>
  <el-tab-pane label="用户列表">
      <hm-complex-table :schema="schema['HmUser']"
                      :columns="showUserColumns"
                      :filters="userFilters"
                      :includes="userIncludes"
                      :refers="userRefers"
                      :options="userOptions"
                      :userDefined="userDefined"></hm-complex-table>
  </el-tab-pane>
</el-tabs>
   </el-main>
</el-container>
  </el-container>
</template>

<script>
  import HmComplexTable from './HmComplexTable.vue'
  import schema from '../../schemas/hm_org_schema'

  export default {
    name: 'HmComplexTableIndex',
    // 继承其他组件
    extends: {},
    // 使用其它组件
    components: {
      'hm-complex-table': HmComplexTable
    },
    data() {
      return {
           radio: '1',
           radio1: '1',
        props: {
          label: 'name',
          children: 'zones'
        },
        count: 1,
        showUserColumns: [
          { name: '用户名', codeCamel: 'mobile', isSort:false },
          { name: '账号', codeCamel: 'loginid', isSort:false },
          { name: '分部', codeCamel: 'loginid', isSort:false },
          { name: '部门', codeCamel: 'loginid', isSort:false },
        ],
        userFilters: [
          { placeholder: '过滤手机号', 'mobile': { 'like': '' }, isShow: true },
          { placeholder: '过滤用户名', 'username': { 'equalTo': '' }, isShow: true },
          { placeholder: ['安全级别大于', '安全级别小于'], 'security_level': { 'greaterThanOrEqualTo': '', 'lessThanOrEqualTo': '' }, isShow: true }
        ],
        userIncludes: {
          'hm_user': {
            includes: ['user_id']
          }
        },
        userRefers: {
          'auth_token': {
            includes: ['userId']
          }
        }
      }
    },
    filters: {
    },
    created() {
      this.schema = schema
      this.userOptions = {
        pageSize: 10,
        sortItem: 'create_time',
        sortOrder: 'desc',
        changeValue: {
          username: { 1: 'Hm-isChecked', 0: 'Hm-noChecked' }
        },
        newData: {
          isShow: true,
          showUserColumns: [
            { name: '姓名', codeCamel: 'username', widgetType: 1 },
            { name: '登录ID', codeCamel: 'loginid', widgetType: 1 },
            { name: '类型', codeCamel: 'type', widgetType: 1 }
          ],
          showUserButtons: [],
          formSchema: schema['HmUser'],
          layout: { left: 0, middle: 24, right: 0 },
          tips: {},
          formStyle: {},
          formRefers: {},
          foreignFormFields: [],
          formRelates: []
        },
        editData: {
          isShow: true,
          showUserColumns: [{ name: '姓名', codeCamel: 'username', widgetType: 1 }],
          showUserButtons: [],
          formSchema: schema['HmUser'],
          layout: { left: 0, middle: 24, right: 0 },
          tips: {},
          formStyle: {},
          formRefers: {},
          foreignFormFields: [],
          formRelates: []
        },
        showDetail: {
          isShow: true
        },
        cellStyle: {},
        titleButtonStyle: {},
        tableStyle: { width: '100%' },
        isShowPagination: true,
        isShowSearch: true,
        showRefresh: true,
        showExport: true,
        showDeleteButton: true,
        buttonGroup: false,
        showSelection: true,
        showOverflowTooltip: true,
        tableCurrentChange(value) {}
        // dataProcessing(value, params, definedOperate) {}, // 处理返回后的数据,必须return 处理后的数据
        // promiseProcessing(value, params, definedOperate) {} // 处理返回后的数据,必须return Promise对象
      }
      this.userDefined = {
        definedParams(params, operate) {
          return params
        },
        definedOperate: [
          { type: 'select', label: '', placeholder: '类型', options: [{ label: '姓名', code: 'username' }, { label: '登录ID', code: 'loginid' }], value: '' },
          { type: 'input', label: '', placeholder: '邮箱', code: 'email', value: '' },
          { type: 'datetime', label: '', placeholder: '创建时间', code: 'createTime', value: '' }
        ],
        definedOperation: [{ label: '测试', func: this.dropDown }],
        definedEdit() {

        },
        definedNew() {

        },
        definedDetail() {

        },
        BatchRemove() {
          console.log('BatchRemove')
        }
        // pretreatment() {}
      }
    },
    methods: {
      method1() {
        this.dialogFormVisible = false
        console.log('method1')
      },
      dropDown(value) {
        console.log('输出一些东西', value)
      },
      statusFunc() {
  
      },
        handleCheckChange(data, checked, indeterminate) {
        console.log(data, checked, indeterminate);
      },
      handleNodeClick(data) {
        console.log(data);
      },
      loadNode(node, resolve) {
        if (node.level === 0) {
          return resolve([{ name: 'region1' }, { name: 'region2' }]);
        }
        if (node.level > 3) return resolve([]);

        var hasChild;
        if (node.data.name === 'region1') {
          hasChild = true;
        } else if (node.data.name === 'region2') {
          hasChild = false;
        } else {
          hasChild = Math.random() > 0.5;
        }

        setTimeout(() => {
          var data;
          if (hasChild) {
            data = [{
              name: 'zone' + this.count++
            }, {
              name: 'zone' + this.count++
            }];
          } else {
            data = [];
          }
          resolve(data);
        }, 500)
      }
    }
  }
</script>
