# For Dev deployment

- Step 1:
    - Chuyển sang nhánh `deploy_ziichat_flutter_ui` sync code mới nhất về từ develop
- Step 2:
    - cd vào thư mục `widgetbook` và chạy lệnh `dart run build_runner build -d`,
      để build phiên bản mới nhất của widgetbook
- Step 3:
    - Chạy lệnh `flutter build web --web-renderer auto --release`
- Step 4:
    - Từ thư mục ziichat-flutter-ui 
    - Chạy lệnh `cp -r assets widgetbook/build/web/assets/packages/ziichat_ui`
    - Để copy thư mục assets chính của project vào trong thư mục `widgetbook/build/web/assets/packages/ziichat_ui` (Tránh việc mất assets khi deploy)
      
    ![Screenshot 2024-08-16 at 13 08 36](https://github.com/user-attachments/assets/7d244201-7e81-464c-96ac-39d1f5bf4d59)

- Step 5:
   - Copy toàn bộ thư mục trong thư mục `build/web` vào trong nhánh `ziichat-flutter-ui` của repo `https://github.com/ziichatlabs/development.tools`
    from

    ![image](https://github.com/user-attachments/assets/1076b73d-938f-4b57-b299-f5ee598d94ca)

    to

    ![image](https://github.com/user-attachments/assets/5ec90464-8d25-4b2d-8dba-3d6e33fb5673)

    
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
- Truy cập vào deploy domain (https://ziichatlabs.github.io/development.tools/) bằng trình duyệt bất kỳ trên điện thoại.



