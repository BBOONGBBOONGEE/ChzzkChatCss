# ChzzkChatCss
치지직 공식 채팅 오버레이의 디자인을 css를 통해 바꿀 수 있게 간단하게 구성해봤습니다.

아래 내용을 복사하여 OBS의 치지직 채팅 오버레이 브라우저 소스의 사용자 지정 CSS 부분에 입력하시면 됩니다.
글꼴을 바꾸고 싶으신 경우 폰트리스트 중 하나를 골라 --user-font-family 옆의 작은따옴표 부분을 바꿔주시면 됩니다.

------------------------------------------------------------------------------------------------------

/* 사용자 설정 (폰트 크기 및 폰트 이름 선택) */
:root {
    --user-font-size: 24px; /* 사용자가 설정할 폰트 크기 */
    --user-font-family: 'TTLaundryGothicB'; /* 사용자가 설정할 폰트 이름 아래에서 복붙하기 */
}
/* 추가된 폰트 리스트 (폰트 이름) */
/* 
- 'GoDoM' (고도체 (기본 글꼴))
- 'GyeonggiTitleM' (경기천년제목)
- 'NPSfontBold' (국민연금체)
- 'SDSamliphopangche_Basic' (삼립호빵체)
- 'KBIZHanmaumGothic' (KBIZ한마음고딕체)
- 'KCC-Hanbit' (KCC한빛체)
- 'SeoulNamsanM' (서울남산체)
- 'TTLaundryGothicB' (런드리고딕체)
*/

/* 다른 웹 폰트 적용 */

@font-face {
  font-family: 'GodoM'; /* 고도체 (기본 글꼴) */
  font-style: normal;
  font-weight: 400;
  src: url('//fastly.jsdelivr.net/korean-webfonts/1/corps/godo/Godo/GodoM.woff2') format('woff2'), url('//fastly.jsdelivr.net/korean-webfonts/1/corps/godo/Godo/GodoM.woff') format('woff');
}

@font-face {
    font-family: 'GyeonggiTitleM'; /* 경기천년제목 */
    src: url('https://fastly.jsdelivr.net/gh/projectnoonnu/noonfonts_one@1.0/GyeonggiTitleM.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}

@font-face {
    font-family: 'NPSfontBold'; /* 국민연금체 */
    src: url('https://fastly.jsdelivr.net/gh/projectnoonnu/noonfonts_2310@1.0/NPSfontBold.woff2') format('woff2');
    font-weight: 700;
    font-style: normal;
}

@font-face {
    font-family: 'SDSamliphopangche_Basic'; /* 삼립호빵체 */
    src: url('https://fastly.jsdelivr.net/gh/projectnoonnu/noonfonts-20-12@1.0/SDSamliphopangche_Basic.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}

@font-face {
    font-family: 'KBIZHanmaumGothic'; /* KBIZ한마음고딕체 */
    src: url('https://fastly.jsdelivr.net/gh/projectnoonnu/noonfonts_one@1.0/KBIZHanmaumGothic.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}

@font-face {
    font-family: 'KCC-Hanbit'; /* KCC한빛체 */
    src: url('https://fastly.jsdelivr.net/gh/projectnoonnu/2403-2@1.0/KCC-Hanbit.woff2') format('woff2');
    font-weight: normal;
    font-style: normal;
}

@font-face {
    font-family: 'SeoulNamsanM'; /* 서울남산체 */
    src: url('https://fastly.jsdelivr.net/gh/projectnoonnu/noonfonts_two@1.0/SeoulNamsanM.woff') format('woff');
    font-weight: normal;
    font-style: normal;
}

@font-face {
    font-family: 'TTLaundryGothicB'; /* 런드리고딕체 */
    src: url('https://fastly.jsdelivr.net/gh/projectnoonnu/2403-2@1.0/TTLaundryGothicB.woff2') format('woff2');
    font-weight: 700;
    font-style: normal;
}

/* 전체 스타일 설정 */
body {
    font-family: var(--user-font-family, 'NPSfontBold'), -apple-system, BlinkMacSystemFont, "Apple SD Gothic Neo", Helvetica, Arial, sans-serif;
}

/* 메시지를 감싸는 박스 디자인 설정 */
.live_overlay_message__lLCT1 {
    background-color: rgba(0, 0, 0, 0.35);
    border-radius: 15px;
    width: 100%;
    max-width: 100%;
}

/* 채팅간 간격 설정 */
.live_overlay_item__Sg18i {
    margin-bottom: 3px;
}

/* 글꼴 설정(위에서 설정했다면 안 바꿔도 됩니다.) */
.live_chatting_message_wrapper__xpYre {
    overflow-wrap: anywhere;
    word-break: break-all;
    font-size: var(--user-font-size, 20px); /* 사용자가 설정한 폰트 크기 */
}

/* 닉네임 스타일 및 외곽선 설정 */
.live_chatting_username_container__m1-i5 {
    margin-bottom: 4px; /* 닉네임과 채팅 간의 간격 */
    text-overflow: ellipsis;
    display: inline-block;
    width: 100%; /* 닉네임이 줄을 차지하도록 설정 */
    text-shadow:
        -1px -1px 1px #000,
         1px -1px 1px #000,
        -1px  1px 1px #000,
         1px  1px 1px #000,
        -1px  0   1px #000,
         1px  0   1px #000,
         0   -1px 1px #000,
         0    1px 1px #000;

}

/* 텍스트의 여백, 간격을 조정합니다. */
.live_chatting_message_container__vrI-y.live_chatting_message_is_overlay__cALCf .live_chatting_message_wrapper__xpYre {
    font-size: var(--user-font-size, 20px);
    line-height: 32px;
    padding: 8px 13px;
}

/* 메시지 색 및 외곽선 설정 */
.live_chatting_message_container__vrI-y.live_chatting_message_is_overlay__cALCf .live_chatting_message_text__DyleH {
    color: #fff;
    text-shadow:
        -1px -1px 1px #000,
         1px -1px 1px #000,
        -1px  1px 1px #000,
         1px  1px 1px #000,
        -1px  0   1px #000,
         1px  0   1px #000,
         0   -1px 1px #000,
         0    1px 1px #000;

}
