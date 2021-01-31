# 目前已知 API

## 综合信息门户

> one.hfut.edu.cn

| 名称         | API                                                    | 参数                                                   | 注释           |
| ------------ | ------------------------------------------------------ | ------------------------------------------------------ | -------------- |
| 用户信息     | /api/center/user/selectUserSimplifyInfoForHall         |                                                        |                |
| 一卡通余额   | /api/operation/thirdPartyApi/schoolcard/balance        | sno=学号/工号                                          |                |
| 未还图书     | /api/operation/library/getBorrowNum                    |                                                        |                |
| 预约图书     | /api/operation/library/getSubscribeNum                 |                                                        |                |
| 用户详细信息 | /api/center/user/selectUserInfoForHall                 |                                                        |                |
| 浏览量       | /api/aggr/aggrgateway/getCount                         | code=PC_CAMPUS_PORTAL                                  |                |
| 课表         | /api/operation/course-timetable/search/学号/YYYY-MM-DD |                                                        | 里面有教师工号 |
| 业务系统链接 | /api/aggr/subject/sublayer                             | gateCode=PC_CAMPUS_PORTAL&subCode=fast-channel&type=15 |                |
| 新闻类型     | /api/aggr/subject/sublayer                             | gateCode=PC_CAMPUS_PORTAL&subCode=public-information   |                |
| 新闻         | /api/operation/newsDetails/getPageData                 | type=新闻类型&size=获取的数量&current=当前页面         |                |

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

