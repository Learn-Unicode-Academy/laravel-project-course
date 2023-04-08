# Phân tích database
1. Table categories => Quản lý danh mục
- id : int
- name : varchar(200)
- slug : varchar(200)
- parent_id : int
- created_at: timesstamp
- updated_at: timesstamp

2. Table course => Quản lý khóa học
- id: int
- name: varchar(255)
- slug: varchar(255)
- detail: text
- teacher_id: int => table teacher
- thumbnail: varchar(255)
- price: float
- sale_price: float
- code: varchar(100)
- durations: float
- is_document: tinyint
- support: text
- status: tinyint
- created_at: timesstamp
- updated_at: timesstamp

3. Table lessions => QUản lý các bài giảng
- id: int
- name: varchar(255)
- slug : varchar(255)
- video_id: int => table
- document_id: int => table
- parent_id: int
- is_trail: tinyint
- views: int
- positon: int
- duration: float
- description: text
- created_at: timesstamp
- updated_at: timesstamp

4. Table categories_course => Trung gian liên kết giữa danh mục - khóa học
- id: int
- category_id: int
- course_id: int
- created_at: timesstamp
- updated_at: timesstamp

5. Table teacher => Giảng viên
- id: int
- name: varchar(100)
- slug: varchar(100)
- description: text
- exp: float
- image: varchar(255)
- created_at: timesstamp
- updated_at: timesstamp

6. Table video => Quản lý video bài giảng
- id: int
- name: varchar(255)
- url => varchar(255)
- created_at: timesstamp
- updated_at: timesstamp

7. Table documents => QUản lý tài liệu bài giảng
- id: int
- name: varchar(255)
- url: varchar(255)
- size: float
- created_at: timesstamp
- updated_at: timesstamp

8. Table categories_post => QUản lý danh mục tin tức
- id: ỉnt
- name : varchar(200)
- slug : varchar(200)
- parent_id : int
- created_at: timesstamp
- updated_at: timesstamp

9. Table posts => QUản lý tin tức
- id: ỉnt
- title : varchar(255)
- slug : varchar(255)
- content : text
- exceprt: text
- thumbnail => varchar(255)
- category_id: int => table
- created_at: timesstamp
- updated_at: timesstamp

10. Table students => QUản lý học viên
- id: ỉnt
- name : varchar(100)
- email: varchar(100)
- password: varchar(100)
- phone: varchar(20)
- address: varchar(200)
- status: tinyint(1)
- created_at: timesstamp
- updated_at: timesstamp

11. Table student_course => Trung gian học viên - khóa học
- id: ỉnt
- course_id: int
- student_id: int
- created_at: timesstamp
- updated_at: timesstamp

12. Table orders => QUản lý đơn hàng đăng ký của học viên
- id: int
- student_id: int
- total: float
- status => tinyint(1)
- created_at: timesstamp
- updated_at: timesstamp

13. Table orders_detail => Chi tiết đơn hàng
- id: int
- order_id: id
- course_id: id
- price: float
- created_at: timesstamp
- updated_at: timesstamp

14. Table orders_status => QUản lý trạng thái đơn hàng
- id: int
- name: varchar(200)
- created_at: timesstamp
- updated_at: timesstamp

15. Table users => Quản trị hệ thống
- id: int
- name: varchar(100)
- email: varchar(100)
- password: varchar(100)
- group_id: int
- created_at: timesstamp
- updated_at: timesstamp

16. Table group => QUản trị nhóm người dùng
- id: int
- name: varchar(100)
- permission: text
- created_at: timesstamp
- updated_at: timesstamp

17. Table Modules => Danh sách modules trong trang quản trị
- id: int
- name: varchar(100)
- title: varchar(200)
- role: text

18. Table options => Quản lý các thiết lập
- id: int
- name: varchar(100)
- value: text