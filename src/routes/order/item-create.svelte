<svelte:head>
  <title>상품조회 | 고객사</title>
</svelte:head>

<script>
import { onMount } from 'svelte';

onMount(() => {
  (function( $ ) {
    //스크립트 영역
    $(document).on("click", ".js_deps3", function(e){
      $(this).toggleClass('active')
      // javascript
      //e.target.classList.toggle("active");
    })
    $(document).on("click", "#btn_deps3_all", function(e){
      if($(this).hasClass("active")){
        $(this).removeClass('active');
        $(".js_deps3").removeClass('active')
      }else{
        $(this).addClass('active');
        $(".js_deps3").addClass('active')
      }
      // javascript
      // if(e.target.classList.contains('active')){
      //   e.target.classList.remove('active')
      //   var btns_deps3 = document.querySelectorAll('button.js_deps3');
      //   btns_deps3.forEach(function(el){
      //     el.classList.remove("active")
      //   })
      // }else{
      //   e.target.classList.add('active')
      //   var btns_deps3 = document.querySelectorAll("button.js_deps3");
      //   btns_deps3.forEach(function(el){
      //     el.classList.add("active")
      //   })
      // }
    })
    // //스크립트 영역
  })(jQuery);
});
</script>

<!-- 페이지영역 -->
<main class="contents">
  <div class="con_title">
    <h3>상품조회</h3>
  </div>
  
  <button type="button" class="btn btn-light btn_srch" data-toggle="collapse" data-target="#srch_area" aria-controls="srch_area" aria-expanded="false">
    <img src="/static/images/icon/arr_srch.svg" alt="검색창 여닫이">
  </button>
  <div class="srch_area collapse show" id="srch_area">
    <table class="table_line">
      <caption>Allt에서 관리하는 정보를 조회하기 위한 입력 폼입니다.</caption>
      <colgroup>
        <col style="width: 10%">
        <col style="width: 40%">
        <col style="width: 10%">
        <col style="width: 40%">
      </colgroup>
      <tbody>
        <tr>
          <th scope="row">
            품목분류
          </th>
          <td colspan="3">
            <div class="rdo_area">
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject0">
                <label for="subject0">선택안함</label>
              </div>
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject1" disabled>
                <label for="subject1" class="disabled">건설/건축자재</label>
              </div>
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject2" checked>
                <label for="subject2">공구</label>
              </div>
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject3">
                <label for="subject3">기계요소</label>
              </div>
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject4">
                <label for="subject4">동력전달/운송기기</label>
              </div>
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject5">
                <label for="subject5">사무/전산용품</label>
              </div>
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject6">
                <label for="subject6">생활잡화</label>
              </div>
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject7">
                <label for="subject7">석유/화학제품</label>
              </div>
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject8">
                <label for="subject8">소방/안전</label>
              </div>
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject9">
                <label for="subject9">실험/계측자재</label>
              </div>
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject10">
                <label for="subject10">유공압/공조</label>
              </div>
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject11">
                <label for="subject11">전기/전자</label>
              </div>
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject12">
                <label for="subject12">청소환경용품</label>
              </div>
              <div class="rdo_label">
                <input type="radio" name="rdo_choice" class="form-control" id="subject13">
                <label for="subject13">포장/판촉/인쇄물</label>
              </div>
            </div>
          </td>
        </tr>
        <tr>
          <th scope="row">
            세부분류
          </th>
          <td colspan="3">
            <div class="chk_area">
              <div class="chk_label">
                <input type="checkbox" class="form-control" id="subdivision1" disabled>
                <label for="subdivision1" class="disabled">전체</label>
              </div>
              <div class="chk_label">
                <input type="checkbox" class="form-control" id="subdivision2" checked>
                <label for="subdivision2">금형공구</label>
              </div>
              <div class="chk_label">
                <input type="checkbox" class="form-control" id="subdivision3">
                <label for="subdivision3">작업공구</label>
              </div>
              <div class="chk_label">
                <input type="checkbox" class="form-control" id="subdivision4">
                <label for="subdivision4">용접기자재</label>
              </div>
              <div class="chk_label">
                <input type="checkbox" class="form-control" id="subdivision5">
                <label for="subdivision5">절단절삭공구</label>
              </div>
              <div class="chk_label">
                <input type="checkbox" class="form-control" id="subdivision6">
                <label for="subdivision6">진동/엔진공구</label>
              </div>
            </div>
          </td> 
        </tr>
        <tr>
          <th scope="row">상품코드</th> 
          <td>
            <input type="text" class="form-control frog" style="width: 19.2rem">
          </td>
          <th scope="row">상품명</th> 
          <td >
            <input type="text" class="form-control" style="width: 19.2rem">
          </td>
        </tr>
      </tbody>
    </table>
    <div class="btn_box">
      <button type="button" class="btn btn-secondary line">초기화</button>
      <button type="button" class="btn btn-secondary">조회</button>
    </div>
  </div>
  <div class="wj-content_wrap">
    <!-- <div class="deps3_area">
      <button type="button" class="btn_deps3" id="btn_deps3_all">전체선택</button>
      <button type="button" class="btn_deps3 active" id="btn_deps3_all">전체해제</button>
      <button type="button" class="js_deps3 btn_deps3">금형공구</button>
      <button type="button" class="js_deps3 btn_deps3">작업공구</button>
      <button type="button" class="js_deps3 btn_deps3">용접기자재</button>
      <button type="button" class="js_deps3 btn_deps3 active">절단절삭공구</button>
      <button type="button" class="js_deps3 btn_deps3">진동/엔진공구</button>
      <button type="button" class="js_deps3 btn_deps3">노트/메모/수첩</button>
      <button type="button" class="js_deps3 btn_deps3">데스크용품</button>
      <button type="button" class="js_deps3 btn_deps3">도서</button>
      <button type="button" class="js_deps3 btn_deps3">메모리카드</button>
      <button type="button" class="js_deps3 btn_deps3">명찰/플레이트</button>
      <button type="button" class="js_deps3 btn_deps3">복사/전산용지/지류</button>
      <button type="button" class="js_deps3 btn_deps3">봉투류</button>
      <button type="button" class="js_deps3 btn_deps3">사무기기</button>
      <button type="button" class="js_deps3 btn_deps3">서식/장부</button>
      <button type="button" class="js_deps3 btn_deps3">스마트기기</button>
      <button type="button" class="js_deps3 btn_deps3">전산소모품</button>
      <button type="button" class="js_deps3 btn_deps3">컴퓨터/주변기기</button>
      <button type="button" class="js_deps3 btn_deps3">프린터소모품</button>
      <button type="button" class="js_deps3 btn_deps3">필기구</button>
      <button type="button" class="js_deps3 btn_deps3">화방/제도/교구</button>
    </div> -->
    <div class="btn_box between">
      <div class="flex_box">
        <button type="button" class="btn btn-light">장바구니 담기</button>
        <button type="button" class="btn btn-light">바로 구매하기</button>
      </div>
      <div class="flex_box">
        <!-- <select name="" class="form-control">
          <option value="">20개씩보기</option>
        </select> 
        <button type="button" class="btn btn-light">이미지보기/감추기</button>
        <button type="button" class="btn btn-light">관심품목 등록</button>
        <button type="button" class="btn btn-light">신규품목신청</button> -->
        <button type="button" class="btn btn-light">Excel 다운로드</button>
        <button type="button" class="btn btn-light btn_icon">
          <img src="/static/images/icon/ico_select_column.svg" alt="컬럼선택">
        </button>
      </div>
    </div>

    <!-- wijmo area -->
    <div id="contentGridEl" class="wj-control wj-content wj-flexgrid" style="position: relative;">
      <div style="position: absolute; top: 50%; transform: translateY(-50%); width: 100%; height: auto; font-size:50px; text-align: center;">
        wijmo area
        <div class="btn_box">
          <button type="button" class="btn btn-light" data-toggle="modal" data-target="#manufactureSearchModal">제조사검색</button>
          <button type="button" class="btn btn-light" data-toggle="modal" data-target="#itemDetailsModal">품목상세정보</button>
          <button type="button" class="btn btn-light" data-toggle="modal" data-target="#buyNowModal">바로구매</button>
        </div>
        <span style="font-size: 14px;">버튼 디자인 추가</span>
        <div class="btn_box">
          <button type="button" class="btn btn-light btn_icon buy"></button>
          <button type="button" class="btn btn-light btn_icon cart"></button>
        </div>
      </div>
    </div>
    <!-- //wijmo area -->
  </div>
</main>
<!-- //페이지영역 -->

<!-- 
하단 모달 활성화 버튼
<button type="button" class="btn btn-light" data-toggle="modal" data-target="#manufactureSearchModal">제조사검색</button>
<button type="button" class="btn btn-light" data-toggle="modal" data-target="#itemDetailsModal">품목상세정보</button>
<button type="button" class="btn btn-light" data-toggle="modal" data-target="#buyNowModal">바로구매</button>
 -->
<!-- 제조사검색 Modal -->
<div class="modal fade" id="manufactureSearchModal" tabindex="-1" role="dialog" aria-hidden="true">
  <div class="modal-dialog modal_md modal-dialog-centered" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title">제조사검색</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true"><img src="/static/images/icon/pop_close.svg" alt="close"></span>
        </button>
      </div>
      <div class="modal-body">
        <table class="table_line">
          <caption>Allt에서 관리하는 정보를 조회하기 위한 입력 폼입니다.</caption>
          <colgroup>
            <col style="width: 21.5%">
            <col style="width: 28.5%">
            <col style="width: 21.5%">
            <col style="width: 28.5%">
          </colgroup>
          <tbody>
            <tr>
              <th scope="row">
                제조사코드
              </th>
              <td>
                <input type="text" class="form-control" value="홍길동" style="width: 10rem">
              </td>
              <th scope="row">
                제조사명
              </th>
              <td>
                <input type="text" class="form-control" value="부서명" style="width: 10rem">
              </td>
            </tr>
          </tbody>
        </table>
        <div class="btn_box mt8">
          <button type="button" class="btn btn-light btn_srch_left">조회</button>
        </div>
        <!-- wijmo area -->
        <div class="wj-control wj-content wj-flexgrid mt32" style="position: relative; height: 17.4rem;">
          <div style="position: absolute; top: 50%; transform: translateY(-50%); width: 100%; height: auto; font-size:50px; text-align: center;">
            wijmo area
          </div>
        </div>
        <!-- //wijmo area -->
      </div>
      <div class="modal-footer btn_box">
        <button type="button" class="btn btn-secondary line" data-dismiss="modal">닫기</button>
      </div>
    </div>
  </div>
</div>

<!-- 품목상세정보 Modal -->
<div class="modal fade" id="itemDetailsModal" tabindex="-1" role="dialog" aria-hidden="true">
  <div class="modal-dialog modal_lg modal-dialog-centered" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title">품목상세정보</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true"><img src="/static/images/icon/pop_close.svg" alt="close"></span>
        </button>
      </div>
      <div class="modal-body">
        <div class="flex_box">
          <!-- 썸네일 정보 있음 -->
          <div class="tableWithImg_box">
            <img src="/static/images/test/temp_item1.png" alt="상품">
          </div>
          <!-- //썸네일 정보 있음 -->
          <table class="table_line">
            <caption>Allt에서 관리하는 정보를 조회하기 위한 입력 폼입니다.</caption>
            <colgroup>
              <col style="width: 21.5%">
              <col style="width: 28.5%">
              <col style="width: 21.5%">
              <col style="width: 28.5%">
            </colgroup>
            <tbody>
              <tr>
                <th scope="row">배송지 정보</th>
                <td colspan="3">1차분류 &gt; 2차분류 &gt; 3차분류 &gt; 4차분류</td>
              </tr>
              <tr>
                <th scope="row">휴대폰</th>
                <td>2000001100</td>
                <th scope="row">거래유형</th>
                <td>직납</td>
              </tr>
              <tr>
                <th scope="row">품명</th>
                <td colspan="3">프리즈마팁&amp;전극</td>
              </tr>
              <tr>
                <th scope="row">규격</th>
                <td colspan="3">P-80(1.8)/SET=10조</td>
              </tr>
            </tbody>
          </table>
        </div>
        <table class="table_line mt32">
          <caption>Allt에서 관리하는 정보를 조회하기 위한 입력 폼입니다.</caption>
          <colgroup>
            <col style="width: 21.5%">
            <col style="width: 28.5%">
            <col style="width: 21.5%">
            <col style="width: 28.5%">
          </colgroup>
          <tbody>
            <tr>
              <th scope="row">제조사</th>
              <td>CRETOS</td>
              <th scope="row">모델번호</th>
              <td>CRETOS</td>
            </tr>
            <tr>
              <th scope="row">단위</th>
              <td>조</td>
              <th scope="row">원산지</th>
              <td>대한민국</td>
            </tr>
            <tr>
              <th scope="row">Catalog담당</th>
              <td>김명규</td>
              <th scope="row">Sourcing담당</th>
              <td>김명규</td>
            </tr>
            <tr>
              <th scope="row">
                첨부파일
              </th>
              <td colspan="3">
                <ul class="file_list">
                  <li>
                    <a href="#" class="link_file">프리즈마팁&amp;전극.pdf</a>
                    <span class="txt_info1">12MB</span>
                    <span class="txt_info2">상태</span>
                  </li>
                  <li>
                    <a href="#"  class="link_file">FH813SZY.PNG</a>
                    <span class="txt_info1">7MB</span>
                    <span class="txt_info2">상태</span>
                  </li>
                  <li>
                    <a href="#"  class="link_file">SETA3870SZY_1.jpg</a>
                    <span class="txt_info1">7MB</span>
                    <span class="txt_info2">상태</span>
                  </li>
                  <li>
                    <a href="#"  class="link_file">SETA3870SZY_1.jpg</a>
                    <span class="txt_info1">2.64MB</span>
                    <span class="txt_info2">상태</span>
                  </li>
                </ul>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      <div class="modal-footer btn_box">
        <button type="button" class="btn btn-secondary line" data-dismiss="modal">닫기</button>
      </div>
    </div>
  </div>
</div>

<!-- 바로구매 Modal -->
<div class="modal fade" id="buyNowModal" tabindex="-1" role="dialog" aria-hidden="true">
  <div class="modal-dialog modal_lg modal-dialog-centered" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title">주문정보 입력</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true"><img src="/static/images/icon/pop_close.svg" alt="close"></span>
        </button>
      </div>
      <div class="modal-body">
        <table class="table_line">
          <caption>Allt에서 관리하는 정보를 조회하기 위한 입력 폼입니다.</caption>
          <colgroup>
            <col style="width: 21.5%">
            <col style="width: 28.5%">
            <col style="width: 21.5%">
            <col style="width: 28.5%">
          </colgroup>
          <tbody>
            <tr>
              <th scope="row">
                인수자
              </th>
              <td>
                <input type="text" class="form-control" value="홍길동" style="width: 17.6rem">
              </td>
              <th scope="row">
                부서
              </th>
              <td>
                <input type="text" class="form-control" value="관리팀" style="width: 17.6rem">
              </td>
            </tr>
            <tr>
              <th scope="row">
                휴대폰
              </th>
              <td>
                <div class="flex_box">
                  <select class="form-control" style="width: 5.6rem;">
                    <option value="010">010</option>
                  </select>
                  <span class="half_frog">-</span>
                  <input type="text" value="2222" class="form-control half_frog" style="width: 4.8rem">
                  <span class="half_frog">-</span>
                  <input type="text" value="2222" class="form-control half_frog" style="width: 4.8rem">
                </div>
              </td>
              <th scope="row">
                연락처
              </th>
              <td>
                <div class="flex_box">
                  <select class="form-control" style="width: 5.6rem;">
                    <option value="010">010</option>
                  </select>
                  <span class="half_frog">-</span>
                  <input type="text" value="2222" class="form-control half_frog" style="width: 4.8rem">
                  <span class="half_frog">-</span>
                  <input type="text" value="2222" class="form-control half_frog" style="width: 4.8rem">
                </div>
              </td>
            </tr>
            <tr>
              <th scope="row">
                선입고여부
              </th> 
              <td>
                <div class="chk_label">
                  <input type="checkbox" class="form-control" id="chk_prearrival">
                  <label for="chk_prearrival">선입고</label>
                </div>
              </td> 
              <th scope="row">
                희망납기일
              </th>
              <td>
                <input type="date" class="form-control" style="width: 10.2rem">
              </td>
            </tr>
            <tr>
              <th scope="row">
                납품장소
              </th>
              <td colspan="3">
                <div class="flex_box">
                  <input type="text" class="form-control" value="07201" style="width: 8.5rem">
                  <button type="button" class="btn btn-light frog">우편번호찾기</button>
                </div>
                <input type="text" class="form-control mt8" value="서울시 영등포구 구로디지털단지로 2112가길 215-20" style="width: 100%" disabled>
                <input type="text" class="form-control mt8" value="스타빌리지 301호" style="width: 100%">
              </td>
            </tr>
            <tr>
              <th scope="row">
                요청사항
              </th>
              <td colspan="3">
                <textarea cols="30" rows="10" style="height: 4.8rem"></textarea>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      <div class="modal-footer btn_box">
        <button type="button" class="btn btn-secondary line" data-dismiss="modal">취소</button>
        <button type="button" class="btn btn-secondary">주문</button>
      </div>
    </div>
  </div>
</div>