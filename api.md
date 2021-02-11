

# 目前已知 API

**下列 API 请求方法如无特殊说明均为 GET**

## 综合信息门户

> one.hfut.edu.cn

| 名称         | API                                                    | 参数                                                         | 注释           |
| ------------ | ------------------------------------------------------ | ------------------------------------------------------------ | -------------- |
| 用户信息     | /api/center/user/selectUserSimplifyInfoForHall         |                                                              |                |
| 一卡通余额   | /api/operation/thirdPartyApi/schoolcard/balance        | sno=学号/工号                                                |                |
| 未还图书     | /api/operation/library/getBorrowNum                    |                                                              |                |
| 预约图书     | /api/operation/library/getSubscribeNum                 |                                                              |                |
| 用户详细信息 | /api/center/user/selectUserInfoForHall                 |                                                              |                |
| 浏览量       | /api/aggr/aggrgateway/getCount                         | code=PC_CAMPUS_PORTAL                                        |                |
| 课表         | /api/operation/course-timetable/search/学号/YYYY-MM-DD |                                                              | 里面有教师工号 |
| 业务系统链接 | /api/aggr/subject/sublayer                             | gateCode=PC_CAMPUS_PORTAL&subCode=fast-channel&type=15       |                |
| 新闻类型     | /api/aggr/subject/sublayer                             | gateCode=PC_CAMPUS_PORTAL&subCode=public-information         |                |
| 新闻         | /api/operation/newsDetails/getPageData                 | type=新闻类型&size=获取的数量&current=页面号                 |                |
| 校区         | /api/operation/emptyClass/campus                       |                                                              |                |
| 教室类型     | /api/operation/emptyClass/roomType                     |                                                              |                |
| 教学楼编号   | /api/operation/emptyClass/build                        | campus_code=校区                                             |                |
| 查询教室     | /api/operation/emptyClass/room                         | building_code=教学楼编号&current=页面号&size=获取的数量      |                |
| 空教室查询   | /api/operation/emptyClass/getEmptyRoom                 | campus_code=校区类型&building_code=教学楼编号&room_type_code=教室类型&seats=座位数&start_unit=开始节次&end_unit=结束节次&start_date=YYYY-MM-DD&end_date=YYYY-MM-DD |                |

## 工大新闻网

> news.hfut.edu.cn

| 名称 | API       | 参数                                                   | 说明 |
| ---- | --------- | ------------------------------------------------------ | ---- |
| 会议 | /yzhy.jsp | urltype=tree.TreeTempUrl&wbtreeid=1057&date=YYYY-MM-DD |      |

## 图书馆

> lib.hfut.edu.cn

| 名称 | API                       | 参数                     | 说明 |
| ---- | ------------------------- | ------------------------ | ---- |
| 书架 | /opac/show_user_shelf.php | classid=十位数的书架编号 |      |

## 一卡通系统

> 172.31.248.20

| 名称                            | API                        | 参数                                                         | 说明                                                         |
| ------------------------------- | -------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 用户信息                        | /accountcardUser.action    |                                                              |                                                              |
| 查询流水第一步                  | /accounthisTrjn.action     |                                                              |                                                              |
| 查询流水第二步<sup>POST</sup>   | /accounthisTrjn1.action    | account: 账号, inputObject: all, Submit: +%C8%B7+%B6%A8+     | Submit 是查询类型                                            |
| 查询流水第三步<sup>POST</sup>   | /accounthisTrjn2.action    | inputStartDate: YYYYMMDD, inputEndDate: YYYYMMDD             | 不限于 31 天                                                 |
| 查询流水第四步<sup>POST</sup>   | /accounthisTrjn3.action    |                                                              |                                                              |
| 通过页数查询流水<sup>POST</sup> | /accountconsubBrows.action | inputStartDate: YYYYMMDD, inputEndDate: YYYYMMDD, pageNum: 页码 | 此处日期必须与第三步查询一致<small>不明白为什么再 POST 一次日期，莫名其妙</small> |

## 教务系统 API

> jxglstu.hfut.edu.cn

| 名称     | API                                            | 参数                                        | 说明           |
| -------- | ---------------------------------------------- | ------------------------------------------- | -------------- |
| 学生信息 | /eams5-student/ws/student/home-page/students   |                                             |                |
| 成绩     | /eams5-student/for-std/grade/sheet/info/学生ID | semester=                                   | 学生ID不是学号 |
| 课表     | /eams5-student/for-std/course-table/get-data   | bizTypeId=2&semesterId=学期ID&dataId=学生ID |                |

## 其他

> hfut.edu.cn

| 名称 | API        | 参数 | 说明               |
| ---- | ---------- | ---- | ------------------ |
| 校车 | /xcxx.htm  |      | 可以用 pandas 读取 |
| 校历 | /gdxl1.htm |      |                    |
