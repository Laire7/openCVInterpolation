# openCVInterpolation
이미지를 확대한 후, 부드럽게 필터링 후 축소해서 interpolation_area와 다른 interpolation 비교(9월9일2024년)
## Interpolation 종류 비교
### Interpolation_Area
![area](https://github.com/user-attachments/assets/542cfcd8-e355-4471-b4ec-be2dca0363ea)
### Interpolation_Lancos4
![lanc](https://github.com/user-attachments/assets/3e265ab9-dd51-4fef-8b65-0620c1353b46)
### Interpolation_Cubic
![cubic](https://github.com/user-attachments/assets/f32ab9a5-2d02-45e7-b87c-b6f0025a3152)
### Interpolation_Nearest
![near](https://github.com/user-attachments/assets/3e3d3d33-cb25-4575-ba96-f978652bbb17)
## 마우스 이벤트
### <code>cv2.setMouseCallback ('windowName', mouse_callback, [imgName]) </code> <code>mouse_callback(event, x, y, flags, param) </code>
<code>flags</code> 마우스 이벤트와 함께 Ctrl, Shift, Alt등의 키가 눌러졌는지 확인 해준다
<code>param</code> 마우스 이벤트가 어떤 창에 해당 될 것인지 지정. 보통 <code> param[0]</code> (첫 번째)을 사용한다  
## 창 사이즈
### <code>cv2.resize(img, (0,0), fx=float, fy=float, interpolation=cv2.INTER_?)</code>
<code> (0,0) </code> 화면 크기를 지정하는데, (0,0)을 넣으면 화면크기를 <code>fx</code>와 <code>fy</code>크기에 따라 지정 됨
사이즈를 키우기만 하면 보통 이미지가 화면 밖으로 출력되는데, resize는 알아서 이미지가 다 보일 수 있게끔 출력 해 줄 수 있다
## 도형 그리기
### <code> cv2.circle(img, (pt_x, pt_y), radius, line_color, line_thickness)
### <code> cv2.polylines(img, [(pt1_x, pt1_y), [pt2_x, pt2_y], ...], isClosedFigure, line_color, line_thickness, line_type) </code>
