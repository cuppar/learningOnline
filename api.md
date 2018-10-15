# 一般每张表都至少有四个API：c(创建)r(读取)u(更新)d(删除)
# 每个API都有request和response(可能为空)
### 每个API响应response都应该包括三个报文头
- Content-Type: application/json
- Access-Control-Request-Origin: *
- Access-Control-Request-Method: GET, POST, PUT, DELETE, OPTIONS

# API
___
## LEARNING_COMMENT_THUMBUP
___
### create

#### POST /api/comment_thumbup

##### req

```json
{
  "user_id": 1,
  "comment_id": 1
}
```

##### res

```json
{
  "user_id": 1,
  "comment_id": 1
}
```
___

### delete

#### DELETE /api/comment_thumbup?user_id=1&comment_id=1

##### req

N/A

##### res

N/A
___
## LEARNING_EXAM
___
### create

#### POST /api/exams

##### req

```json
{
  "paper": "paper-json",
  "course_id": 1,
  "start_time": "2018-10-1 19:00:00",
  "end_time": "2019-10-1 19:00:00",
  "exam_cost": 100 //分钟
}
```

##### res

```json
{
  "id": 1,
  "paper": "paper-json",
  "course_id": 1,
  "start_time": "2018-10-1 19:00:00",
  "end_time": "2019-10-1 19:00:00",
  "exam_cost": 100 //分钟
}
```
___

### count

#### GET /api/exams/count

##### req

N/A

##### res

```json
{
  "count": 1234
}
```
___

### list

#### GET /api/exams(？size=10&page=2) 
//()内为可选，若无表示返回所有考试信息，若有表示分页返回

##### req

N/A

##### res

```json
[
  {
    "id": 1,
    "paper": "paper-json",
    "course_id": 1,
    "start_time": "2018-10-1 19:00:00",
    "end_time": "2019-10-1 19:00:00",
    "exam_cost": 100 //分钟
  },
  {
    "id": 2,
    "paper": "paper-json",
    "course_id": 1,
    "start_time": "2018-10-1 19:00:00",
    "end_time": "2019-10-1 19:00:00",
    "exam_cost": 100 //分钟
  }  
]
```
___

### query

#### GET /api/exams/:id

##### req

N/A

##### res

```json
{
  "id": 1,
  "paper": "paper-json",
  "course_id": 1,
  "start_time": "2018-10-1 19:00:00",
  "end_time": "2019-10-1 19:00:00",
  "exam_cost": 100 //分钟
}
```
___

### update

#### PUT /api/exams/:id

##### req

```json
{
  "paper": "paper-json",
  "course_id": 1,
  "start_time": "2018-10-1 19:00:00",
  "end_time": "2019-10-1 19:00:00",
  "exam_cost": 100 //分钟
}
```

##### res

```json
{
  "id": 1,
  "paper": "paper-json",
  "course_id": 1,
  "start_time": "2018-10-01 19:00:00",
  "end_time": "2019-10-01 19:00:00",
  "exam_cost": 100 //分钟
}
```
___

### delete

#### DELETE /api/exams/:id

##### req

N/A

##### res

N/A

___
## LEARNING_COMMENT
___
### create

#### POST /api/comment

##### req

```json
{
  "pre_id": 1, //为null表示是一级评论（即评论章节）
  "user_id": 2,
  "content": "comment content",
  "pre_content": "pre comment content",
  "top_time": "2018-10-01 19:00:00",
  "chapter_id": 3,
}
```

##### res

```json
{
  "id": 4,
  "pre_id": 1, //为null表示是一级评论（即评论章节）
  "user_id": 2,
  "content": "comment content",
  "pre_content": "pre comment content",
  "top_time": "2018-10-01 19:00:00",
  "chapter_id": 3,
}
```
___








