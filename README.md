# For Dev deployment

- Step 1:
    - Chuyển sang nhánh `deploy_ziichat_flutter_ui` sync code mới nhất về từ develop
- Step 2:
    - cd vào thư mục `widgetbook` và chạy lệnh `dart run build_runner build -d`,
      để build phiên bản mới nhất của widgetbook
- Step 3:
    - Chạy lệnh `flutter build web --web-renderer auto --release`
- Step 4:
    - Copy toàn bộ thư mục trong thư mục widgetbook/build/web
    vào nhánh ziichat_flutter_ui của repo `https://github.com/ziichatlabs/development.tools/tree/deploy-tool`

    - from

        ![Screenshot 2024-08-16 at 11 08 25](https://github.com/user-attachments/assets/edbf9af2-2ffd-4dea-8616-737e768e3030)

    - to
      
      ![image](https://github.com/user-attachments/assets/cd404712-d6f5-4c26-9e17-173e1bc34830)


- Step 5:
    - Quay lại nhánh `deploy_ziichat_flutter_ui` và copy thư mục
    assets chính của project vào trong thư mục `assets/packages/ziichat_ui` của repo `https://github.com/ziichatlabs/development.tools/tree/deploy-tool` (tại nhánh ziichat_flutter_ui), để tránh trường hợp thiếu assets khi deploy
    - from
      
    ![Screenshot 2024-08-16 at 11 13 42](https://github.com/user-attachments/assets/1c1e1ff6-0eb1-4d27-af02-9815c0b4b376)

    - to

    ![image](https://github.com/user-attachments/assets/22d604bd-aedc-47ed-aa21-a4479c7e424c)

    
- Step 6:
    - Chỉnh sửa đường dẫn trong file index.html vừa mới copy thành
    from
    ```<base href="/">```
    to
    ```<base href="https://ziichatlabs.github.io/development.tools/">``` (Deploy domain)

    ![Screenshot 2024-08-16 at 11 18 47](https://github.com/user-attachments/assets/f7670a2d-eb1c-4afa-bbb3-2484155e6df6)

- Step 7:
    - Commit and push code
 
# For QC
- Step 1:
    - Sau khi truy cập vào deploy domain (https://ziichatlabs.github.io/development.tools/),
      chuột phải chọn Inspect.
      
     ![Screenshot 2024-08-16 at 10 47 42](https://github.com/user-attachments/assets/46f554d0-081b-419c-8b0d-c5ec6e62a90d)
- Step 2:
    - Click vào biểu tượng reponsive ở góc trái cửa sổ inspect
      
     ![Screenshot 2024-08-16 at 10 49 02](https://github.com/user-attachments/assets/6487bf88-d97f-482c-a146-267faeecb959)
    - Giao diện sẽ trông như thế này
      
     ![Screenshot 2024-08-16 at 10 51 19](https://github.com/user-attachments/assets/e3baa430-7f5b-45cc-90e9-fd953928b68b)

- Step 3:
  - Tại đây có thể chọn các thiết bị khác nhau để test cũng như có thể chọn chế độ quay ngang hoặc quay dọc
    
  ![Screenshot 2024-08-16 at 10 52 28](https://github.com/user-attachments/assets/5753c3aa-39a2-4315-90a9-aa4a0a0d173e)

