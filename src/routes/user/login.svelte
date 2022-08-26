<section class="login_contents">
  <div class="tit_wrap">
    <h2 class="tit"><img src="/static/images/allt_logo.svg" alt="allt"></h2>
  </div>
  <div class="container">
    <div class="row no-gutters justify-content-center">
      <div class="col-12 col-md-6 col-lg-4">
        <div class="form_wrap_line">
          <div class="form-group">
            <label for="id" class="login_input_title">아이디</label>
            <input type="text" id="id" style="width: 100%;" class="form-control box"
              placeholder="welcome@email.com" title="아이디" required>
          </div>
          <div class="form-group">
            <label for="pw" class="login_input_title">비밀번호</label>
            <input type="password" id="pw" ref="pap" style="width: 100%;"
              class="form-control box" placeholder="비밀번호를 입력하세요." title="비밀번호" required>
          </div>
          <div class="login_utile">
            <div class="check_area">
              <input type="checkbox" id="id_save">
              <label for="id_save">아이디 저장</label>
            </div>
            <div class="find_area">
              <a href="#">비밀번호 찾기</a>
            </div>
          </div>
          <div class="login_box">
            <button type="submit" class="btn btn_lg btn_primary">로그인</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  /* -------- form_wrap_line -------- */
.login_contents .login_utile {
	display: flex;
	margin-top: 20px;
	justify-content: space-between;
	align-items: center;
}

.login_contents .login_utile .check_area {
	margin: 0;
}

.login_contents .login_utile .find_area {
	display: inline-block;
	font-weight: 500;
	/* font-size: 1.3rem; */
	color: #959595;
}

.login_contents .login_top .btn-group {
	margin-top: 22px;
}
</style>