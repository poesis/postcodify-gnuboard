
Postcodify 그누보드 플러그인
============================

[Postcodify](http://postcodify.poesis.kr/) 새주소 우편번호 검색 API를
그누보드와 쉽게 연동할 수 있도록 만든 플러그인입니다.
이 플러그인을 사용하면 그누보드에서 공식 지원하는 DAUM 우편번호 검색 API를
Postcodify 무료 API로 변경할 수 있습니다.

아래의 설명은 DAUM 우편번호 검색 API로 전환한 버전 (5.0.16 이상) 기준입니다.

전환 과도기 버전 (5.0.14~15) 사용시 정상 작동하지 않을 수도 있습니다.
DAUM 우편번호 검색 API로 전환하지 않은 버전 (5.0.13 이하) 사용하시는 분은
이 플러그인을 설치하지 말고, Postcodify의 [에뮬레이션](http://postcodify.poesis.kr/guide/emulation) 기능을 활용하시기 바랍니다.

그누보드4에서는 jQuery 버전에 따라 작동할 수도 있고 안 될 수도 있습니다.
문제가 있다면 jQuery 1.7 이상으로 업그레이드해 주십시오.


새우편번호 대응 안내
--------------------

그누보드 5.0.41 버전부터 5자리 새우편번호(기초구역번호)를 지원합니다.
새우편번호를 지원하는 버전의 그누보드에서 이 플러그인을 사용하면 자동으로 새우편번호가 입력되며,
그렇지 않은 버전에서는 기존 우편번호가 입력됩니다.

그누보드 버전과 관계없이 특정 포맷의 우편번호 입력이 필요하신 분은 스킨을 수정하셔야 합니다.
`mb_zip`이라는 이름의 입력란이 존재할 경우 새우편번호가 입력되고,
`mb_zip1` 및 `mb_zip2`라는 이름의 입력란이 존재할 경우 기존 우편번호가 입력되니 참고하십시오.


설치 방법 (그누보드5)
---------------------

(1) 그누보드의 `plugin` 폴더 내에 `postcodify`라는 이름의 폴더를 생성합니다.

(2) 플러그인의 `zip.js` 파일을 위에서 생성한 폴더로 복사합니다.

(3) 그누보드에서 다음의 파일들을 찾아

  - `adm/member_form.php`
  - `skin/member/스킨명/register_form.skin.php`
  - 그 밖에 주소입력 기능이 필요한 모든 페이지

아래의 내용을 맨 아래에 추가합니다.

    <script src="<?php echo G5_PLUGIN_URL ?>/postcodify/zip.js"></script>

(4) 회원가입, 회원정보 변경, 관리자 페이지 등에서 우편번호 검색을 해봅니다.


라이센스
--------

이 플러그인은 LGPL v2.1 또는 그 이후 버전에 따라 자유롭게 사용할 수 있습니다.
