# GIT

Trường hợp muốn change lại message khi commit

        git commit –amend -m”message”

## Di chuyển file từ vùng staging về vùng working directory `(staging -> working directory)`

        git restore  --staged <file_name>

Restore toàn bộ các file

        git restore --staged . 

## Di chuyển file từ vùng repository về vùng working directory `(repository -> working directory)`

        git reset HEAD~1

        git reset HEAD ~N

- *Commit đầu tiên không thể bị reset*

- *Nếu muốn reset -> xóa thư mục .git rồi init lại*

## Git Branching

Git sử dụng nhánh (branch) để tạo ra các `phiên bản` riêng của code, tránh ảnh hưởng tới “bản gốc”

Lấy code từ server về

        git pull origin main

        
Ở lesson-01, đã config 

 git config --global init .defaultBranch main 

-> cấu hình: khi khởi tạo, đặt nhánh mặc định là nhánh main

## Một số câu lệnh với nhánh

1. Xem danh sách nhánh

        git brach

- *Lưu ý: cần có ít nhất 1 commit mới hiện danh sách nhánh*

2. Tạo nhánh mới:

        git branch <tên_bracnch>

- *Nhánh mới copy giống hệt nhánh hiện tại*

3. Chuyển sang nhánh mới

        git checkout <tên_branch>

4. Vừa tạo, vừa chuyển sang nhánh mới:

        git checkout -b <tên>

5. Xóa branch

        git branch -D <tên_nhánh>

- *Lưu ý: luôn pull code về trước khi tạo nhánh mới*

## .gitignore file

.gitignore = GitIgnore = Bỏ qua

Dùng bỏ qua các file không cần git theo dõi

1. Ignore file

        <file_name>

2. Ignore folder

        <folder-name> /

# Javascript

### Convention = quy tắc

Code theo 1 format, dễ nhìn

Người khác trong team dễ đọc code

        Snake_case: chưa dùng

        Kebab-case: tên file

        camelCase: tên biến

        PascalCase: tên class

## console.log with ` and ""

        console.log('Toi là Thao');

        console.log("Toi là Phuong Thao");

        console.log(`${variable_name}`);

Let name = "Thao";

console.log(`Toi la ${name}`);

console.log("Toi ten la" + name + " ");

## Object

Gọi là đối tượng

Lưu trữ tập hợp các giá trị vào cùng 1 biến hoặc hằng số

Khai báo

        let/const <ten_object> = {
	        <thuoc_tinh>: <gia_tri>,
	        …
        }

*<thuoc_tinh> : giống quy tắc đặt tên biến*

*<gia_tri> : có kiểu giống biên, hoặc là 1 object khác.*

### Sử dụng

        console.log(“Tên món: ” + food.name);

        console.log(“Chi nhánh: ” + food.
        branch.facility);

        console.log(“Giá: ”, food[“price”]);

        console.log(“Năm khai trương: ”, 
        food[“branch”][“year”]);

### Gán lại

    let student = {

        name: "Thao", 

        role: "student",

        class: {

            name: "K18",

            subject: "Fullstack Automation"
        }

    }

    student.name = "Thao Nguyen"

    console.log(student);

## Mảng

Mảng là một danh sách có thứ tự, lưu nhiều giá trị trong một biến.

### Khai báo

        const arr = ["Thao", "Phuong", 
        "Hien", "Hieu", ,8, true]

        let mixed = [1, "xin chào", true, { 
        name: "Trang" }];

### Truy xuất mảng

Độ dài mảng: length

Lấy phần tử theo index: 
	[0], [1], [2]

        const arr = ["Thao", "Phuong", 
        "Hien", "Hieu", ,8, true]

        console.log("Do dai mang la", arr.
        length);

        console.log("Ten toi la", arr[0]);

## Function

Là hàm

Là đoạn code được đặt tên và có thể tái sử dụng, thực hiện 1 nhiệm vụ hoặc 1 tính toán cụ thể

### Khai báo

        function <nameFunction>() {
            // code
        }

        function sayHelloWorld() {

            console.log("Hello World!");

        }

        sayHelloWorld();

### Parameter

Parameter (tham số) là biến được định nghĩa trong khai báo hàm, dùng để nhận giá trị từ bên ngoài truyền vào.

        function countBeforeHello(n) {
            for (let i = 0; i <= n; i++) {
                console.log(i);
            }
            sayHelloWorld();
        }

        countBeforeHello(10);

### Return value

return value = giá trị trả về của một hàm sau khi thực thi.

Khi bạn gọi hàm, hàm có thể trả về (return) một kết quả để dùng tiếp.

Nếu không return, mặc định hàm sẽ trả về undefined.

        function sum(a, b) {
            const sum = a + b;
            return sum;
        }

        const total = sum(5, 6);
        console.log(total);
        console.log(sum(5, 10));























