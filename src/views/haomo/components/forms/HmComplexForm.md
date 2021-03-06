### 基本使用

```jsx
    <hm-complex-form   :columns="[
                                    { name: 'username', widgetType: 1 }, 
                                    { name: 'securityLevel', widgetType: 5 }, 
                                    { name: 'type', widgetType: 2, options: ['企业', '代理商'] }, 
                                    { name: 'avatar', widgetType: 3 }, 
                                    { name: 'departmentId', widgetType: 4 }, 
                                    { name: 'createTime', widgetType: 6 }
                                 ]"
                        :schema="{
                                   'model': 'HmUser',
                                                   'modelPlural': 'HmUsers',
                                                   'modelCamel': 'hmUser',
                                                   'modelCamelPlural': 'hmUsers',
                                                   'modelUnderscore': 'hm_user',
                                                   'modelUnderscorePlural': 'hm_users',
                                                   'columns': [
                                                     {
                                                       'id': 'o50',
                                                       'objectId': '170A4473-36CC-47E1-96C3-F238F8132AA4',
                                                       'name': '用户名字',
                                                       'code': 'USERNAME',
                                                       'creationDate': '1498990741',
                                                       'creator': 'hm20160509',
                                                       'modificationDate': '1517859502',
                                                       'modifier': 'hm20160509',
                                                       'dataType': 'VARCHAR2(256CHAR)',
                                                       'length': '256',
                                                       'codeCamel': 'username',
                                                       'codeCamelPlural': 'usernames',
                                                       'codeUnderscore': 'username',
                                                       'codeUnderscorePlural': 'usernames',
                                                       'type': 'string'
                                                     },
                                                     {
                                                       'id': 'o51',
                                                       'objectId': '70EC38C6-4AE4-4E79-BA72-29DA2FE50782',
                                                       'name': '登录ID',
                                                       'code': 'LOGINID',
                                                       'creationDate': '1498990741',
                                                       'creator': 'hm20160509',
                                                       'modificationDate': '1498995491',
                                                       'modifier': 'xjq',
                                                       'dataType': 'VARCHAR2(256CHAR)',
                                                       'length': '256',
                                                       'columnMandatory': '1',
                                                       'codeCamel': 'loginid',
                                                       'codeCamelPlural': 'loginids',
                                                       'codeUnderscore': 'loginid',
                                                       'codeUnderscorePlural': 'loginids',
                                                       'type': 'string'
                                                     },
                                                     {
                                                       'id': 'o52',
                                                       'objectId': '4FCE7185-D489-4DED-AA5F-093A4DBC1112',
                                                       'name': '密码',
                                                       'code': 'PASSWORD',
                                                       'creationDate': '1498990741',
                                                       'creator': 'hm20160509',
                                                       'modificationDate': '1498995491',
                                                       'modifier': 'xjq',
                                                       'dataType': 'VARCHAR2(256CHAR)',
                                                       'length': '256',
                                                       'codeCamel': 'password',
                                                       'codeCamelPlural': 'passwords',
                                                       'codeUnderscore': 'password',
                                                       'codeUnderscorePlural': 'passwords',
                                                       'type': 'string'
                                                     },
                                                     {
                                                       'id': 'o53',
                                                       'objectId': '3A897125-CB02-40F5-9BB1-62A9B06553E0',
                                                       'name': '联系电话',
                                                       'code': 'MOBILE',
                                                       'creationDate': '1498990741',
                                                       'creator': 'hm20160509',
                                                       'modificationDate': '1498995491',
                                                       'modifier': 'xjq',
                                                       'dataType': 'VARCHAR2(16CHAR)',
                                                       'length': '16',
                                                       'codeCamel': 'mobile',
                                                       'codeCamelPlural': 'mobiles',
                                                       'codeUnderscore': 'mobile',
                                                       'codeUnderscorePlural': 'mobiles',
                                                       'type': 'string'
                                                     },
                                                     {
                                                       'id': 'o54',
                                                       'objectId': '48B9C079-3CCA-4886-9543-3AE764998E9A',
                                                       'name': '邮箱',
                                                       'code': 'EMAIL',
                                                       'creationDate': '1498990741',
                                                       'creator': 'hm20160509',
                                                       'modificationDate': '1498995491',
                                                       'modifier': 'xjq',
                                                       'dataType': 'VARCHAR2(256CHAR)',
                                                       'length': '256',
                                                       'codeCamel': 'email',
                                                       'codeCamelPlural': 'emails',
                                                       'codeUnderscore': 'email',
                                                       'codeUnderscorePlural': 'emails',
                                                       'type': 'string'
                                                     },
                                                     {
                                                       'id': 'o55',
                                                       'objectId': '533AB6E8-A3D0-473D-9DE6-0D0CABA6731C',
                                                       'name': '头像',
                                                       'code': 'AVATAR',
                                                       'creationDate': '1498990741',
                                                       'creator': 'hm20160509',
                                                       'modificationDate': '1498995491',
                                                       'modifier': 'xjq',
                                                       'dataType': 'VARCHAR2(1024CHAR)',
                                                       'length': '1024',
                                                       'codeCamel': 'avatar',
                                                       'codeCamelPlural': 'avatars',
                                                       'codeUnderscore': 'avatar',
                                                       'codeUnderscorePlural': 'avatars',
                                                       'type': 'string'
                                                     },
                                                     {
                                                       'id': 'o56',
                                                       'objectId': 'EF44AF1F-F6B9-412F-9FF7-AAECD6B5521A',
                                                       'name': '创建时间',
                                                       'code': 'CREATE_TIME',
                                                       'creationDate': '1498990741',
                                                       'creator': 'hm20160509',
                                                       'modificationDate': '1498995491',
                                                       'modifier': 'xjq',
                                                       'dataType': 'DATE',
                                                       'codeCamel': 'createTime',
                                                       'codeCamelPlural': 'createTimes',
                                                       'codeUnderscore': 'create_time',
                                                       'codeUnderscorePlural': 'create_times',
                                                       'type': 'datetime'
                                                     },
                                                     {
                                                       'id': 'o57',
                                                       'objectId': 'CD1BC772-356B-4D14-A40E-28F115F95EEC',
                                                       'name': '更新时间',
                                                       'code': 'LAST_UPDATE_TIME',
                                                       'creationDate': '1498990741',
                                                       'creator': 'hm20160509',
                                                       'modificationDate': '1498995491',
                                                       'modifier': 'xjq',
                                                       'dataType': 'DATE',
                                                       'codeCamel': 'lastUpdateTime',
                                                       'codeCamelPlural': 'lastUpdateTimes',
                                                       'codeUnderscore': 'last_update_time',
                                                       'codeUnderscorePlural': 'last_update_times',
                                                       'type': 'datetime'
                                                     },
                                                     {
                                                       'id': 'o58',
                                                       'objectId': '297D03AE-459D-4991-A459-3449FE893EEB',
                                                       'name': '最后登录时间',
                                                       'code': 'LAST_LOGIN_TIME',
                                                       'creationDate': '1498990741',
                                                       'creator': 'hm20160509',
                                                       'modificationDate': '1498995491',
                                                       'modifier': 'xjq',
                                                       'dataType': 'DATE',
                                                       'codeCamel': 'lastLoginTime',
                                                       'codeCamelPlural': 'lastLoginTimes',
                                                       'codeUnderscore': 'last_login_time',
                                                       'codeUnderscorePlural': 'last_login_times',
                                                       'type': 'datetime'
                                                     },
                                                     {
                                                       'id': 'o59',
                                                       'objectId': '6767F0FE-6C49-46F3-919E-D854C21FCA52',
                                                       'name': '安全级别',
                                                       'code': 'SECURITY_LEVEL',
                                                       'creationDate': '1498990741',
                                                       'creator': 'hm20160509',
                                                       'modificationDate': '1498995491',
                                                       'modifier': 'xjq',
                                                       'dataType': 'NUMBER(11,0)',
                                                       'length': '11',
                                                       'codeCamel': 'securityLevel',
                                                       'codeCamelPlural': 'securityLevels',
                                                       'codeUnderscore': 'security_level',
                                                       'codeUnderscorePlural': 'security_levels',
                                                       'type': 'number'
                                                     },
                                                     {
                                                       'id': 'o60',
                                                       'objectId': 'C4BF570D-C8FC-4B72-919C-78DB3D790171',
                                                       'name': '类型',
                                                       'code': 'TYPE',
                                                       'creationDate': '1498990741',
                                                       'creator': 'hm20160509',
                                                       'modificationDate': '1498995491',
                                                       'modifier': 'xjq',
                                                       'comment': '1:企业，2：代理商',
                                                       'dataType': 'NUMBER(11,0)',
                                                       'length': '11',
                                                       'codeCamel': 'type',
                                                       'codeCamelPlural': 'types',
                                                       'codeUnderscore': 'type',
                                                       'codeUnderscorePlural': 'types',
                                                       'type': 'number'
                                                     }
                                                                                        ]
                                                                                      }"></hm-complex-form>
```

### 指定显示的表单类型及按钮

```vue
<template>
    <hm-complex-form :schema="schema['HmUser']"
                     :columns="showUserColumns"
                     :tableId="tableId"
                     :layout="layout"
                     :buttons="showUserButtons">
                      
    </hm-complex-form>
</template>

<script>
  export default {
    name: 'HmComplexFormIndex',
    data() {
      return {
        schema: {
            'HmUser': {
                'model': 'HmUser',
                'modelPlural': 'HmUsers',
                'modelCamel': 'hmUser',
                'modelCamelPlural': 'hmUsers',
                'modelUnderscore': 'hm_user',
                'modelUnderscorePlural': 'hm_users',
                'columns': [
                  {
                    'id': 'o50',
                    'objectId': '170A4473-36CC-47E1-96C3-F238F8132AA4',
                    'name': '用户名字',
                    'code': 'USERNAME',
                    'creationDate': '1498990741',
                    'creator': 'hm20160509',
                    'modificationDate': '1517859502',
                    'modifier': 'hm20160509',
                    'dataType': 'VARCHAR2(256CHAR)',
                    'length': '256',
                    'codeCamel': 'username',
                    'codeCamelPlural': 'usernames',
                    'codeUnderscore': 'username',
                    'codeUnderscorePlural': 'usernames',
                    'type': 'string'
                  },
                  {
                    'id': 'o51',
                    'objectId': '70EC38C6-4AE4-4E79-BA72-29DA2FE50782',
                    'name': '登录ID',
                    'code': 'LOGINID',
                    'creationDate': '1498990741',
                    'creator': 'hm20160509',
                    'modificationDate': '1498995491',
                    'modifier': 'xjq',
                    'dataType': 'VARCHAR2(256CHAR)',
                    'length': '256',
                    'columnMandatory': '1',
                    'codeCamel': 'loginid',
                    'codeCamelPlural': 'loginids',
                    'codeUnderscore': 'loginid',
                    'codeUnderscorePlural': 'loginids',
                    'type': 'string'
                  },
                  {
                    'id': 'o52',
                    'objectId': '4FCE7185-D489-4DED-AA5F-093A4DBC1112',
                    'name': '密码',
                    'code': 'PASSWORD',
                    'creationDate': '1498990741',
                    'creator': 'hm20160509',
                    'modificationDate': '1498995491',
                    'modifier': 'xjq',
                    'dataType': 'VARCHAR2(256CHAR)',
                    'length': '256',
                    'codeCamel': 'password',
                    'codeCamelPlural': 'passwords',
                    'codeUnderscore': 'password',
                    'codeUnderscorePlural': 'passwords',
                    'type': 'string'
                  },
                  {
                    'id': 'o53',
                    'objectId': '3A897125-CB02-40F5-9BB1-62A9B06553E0',
                    'name': '联系电话',
                    'code': 'MOBILE',
                    'creationDate': '1498990741',
                    'creator': 'hm20160509',
                    'modificationDate': '1498995491',
                    'modifier': 'xjq',
                    'dataType': 'VARCHAR2(16CHAR)',
                    'length': '16',
                    'codeCamel': 'mobile',
                    'codeCamelPlural': 'mobiles',
                    'codeUnderscore': 'mobile',
                    'codeUnderscorePlural': 'mobiles',
                    'type': 'string'
                  },
                  {
                    'id': 'o54',
                    'objectId': '48B9C079-3CCA-4886-9543-3AE764998E9A',
                    'name': '邮箱',
                    'code': 'EMAIL',
                    'creationDate': '1498990741',
                    'creator': 'hm20160509',
                    'modificationDate': '1498995491',
                    'modifier': 'xjq',
                    'dataType': 'VARCHAR2(256CHAR)',
                    'length': '256',
                    'codeCamel': 'email',
                    'codeCamelPlural': 'emails',
                    'codeUnderscore': 'email',
                    'codeUnderscorePlural': 'emails',
                    'type': 'string'
                  },
                  {
                    'id': 'o55',
                    'objectId': '533AB6E8-A3D0-473D-9DE6-0D0CABA6731C',
                    'name': '头像',
                    'code': 'AVATAR',
                    'creationDate': '1498990741',
                    'creator': 'hm20160509',
                    'modificationDate': '1498995491',
                    'modifier': 'xjq',
                    'dataType': 'VARCHAR2(1024CHAR)',
                    'length': '1024',
                    'codeCamel': 'avatar',
                    'codeCamelPlural': 'avatars',
                    'codeUnderscore': 'avatar',
                    'codeUnderscorePlural': 'avatars',
                    'type': 'string'
                  },
                  {
                    'id': 'o56',
                    'objectId': 'EF44AF1F-F6B9-412F-9FF7-AAECD6B5521A',
                    'name': '创建时间',
                    'code': 'CREATE_TIME',
                    'creationDate': '1498990741',
                    'creator': 'hm20160509',
                    'modificationDate': '1498995491',
                    'modifier': 'xjq',
                    'dataType': 'DATE',
                    'codeCamel': 'createTime',
                    'codeCamelPlural': 'createTimes',
                    'codeUnderscore': 'create_time',
                    'codeUnderscorePlural': 'create_times',
                    'type': 'datetime'
                  },
                  {
                    'id': 'o57',
                    'objectId': 'CD1BC772-356B-4D14-A40E-28F115F95EEC',
                    'name': '更新时间',
                    'code': 'LAST_UPDATE_TIME',
                    'creationDate': '1498990741',
                    'creator': 'hm20160509',
                    'modificationDate': '1498995491',
                    'modifier': 'xjq',
                    'dataType': 'DATE',
                    'codeCamel': 'lastUpdateTime',
                    'codeCamelPlural': 'lastUpdateTimes',
                    'codeUnderscore': 'last_update_time',
                    'codeUnderscorePlural': 'last_update_times',
                    'type': 'datetime'
                  },
                  {
                    'id': 'o58',
                    'objectId': '297D03AE-459D-4991-A459-3449FE893EEB',
                    'name': '最后登录时间',
                    'code': 'LAST_LOGIN_TIME',
                    'creationDate': '1498990741',
                    'creator': 'hm20160509',
                    'modificationDate': '1498995491',
                    'modifier': 'xjq',
                    'dataType': 'DATE',
                    'codeCamel': 'lastLoginTime',
                    'codeCamelPlural': 'lastLoginTimes',
                    'codeUnderscore': 'last_login_time',
                    'codeUnderscorePlural': 'last_login_times',
                    'type': 'datetime'
                  },
                  {
                    'id': 'o59',
                    'objectId': '6767F0FE-6C49-46F3-919E-D854C21FCA52',
                    'name': '安全级别',
                    'code': 'SECURITY_LEVEL',
                    'creationDate': '1498990741',
                    'creator': 'hm20160509',
                    'modificationDate': '1498995491',
                    'modifier': 'xjq',
                    'dataType': 'NUMBER(11,0)',
                    'length': '11',
                    'codeCamel': 'securityLevel',
                    'codeCamelPlural': 'securityLevels',
                    'codeUnderscore': 'security_level',
                    'codeUnderscorePlural': 'security_levels',
                    'type': 'number'
                  },
                  {
                    'id': 'o60',
                    'objectId': 'C4BF570D-C8FC-4B72-919C-78DB3D790171',
                    'name': '类型',
                    'code': 'TYPE',
                    'creationDate': '1498990741',
                    'creator': 'hm20160509',
                    'modificationDate': '1498995491',
                    'modifier': 'xjq',
                    'comment': '1:企业，2：代理商',
                    'dataType': 'NUMBER(11,0)',
                    'length': '11',
                    'codeCamel': 'type',
                    'codeCamelPlural': 'types',
                    'codeUnderscore': 'type',
                    'codeUnderscorePlural': 'types',
                    'type': 'number'
                  }
                ]
              }
        },
        showUserColumns: [{ name: 'username', widgetType: 1 }, { name: 'securityLevel', widgetType: 5 }, { name: 'type', widgetType: 2, options: ['企业', '代理商'] }, { name: 'avatar', widgetType: 3 }, { name: 'departmentId', widgetType: 4 }, { name: 'createTime', widgetType: 6 }],
                // 要显示按钮 暂只支持确定、保存、取消、提交、重置
        showUserButtons: ['确定', '取消'],
        layout: { left: 0, middle: 12, right: 12 }
      }
    },
    created() {
      this.schema = schema
      this.tableId = '0e26566e953449a7a7500c34be39fd26'
    }
  }
</script>


```