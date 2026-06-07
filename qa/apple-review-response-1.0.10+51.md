# Apple App Review 1.2 (UGC) 재제출용 답변 / 메모 모음

> Submission ID 907894f3-a78d-4cdf-b1ec-5218da9542d4 의 1.0.10 (59) 재제출 시 사용
>
> 이전 거부 사유: 4번째 거부(2026-05-11)에서 18+ age rating 만 단독 사유. 그 외 모든 precaution 충족 인정.
> 대응: **연령 등급 16+ 로 조정** + 작성자 식별 정보 노출 강화 (nicknameWithCode, AuthorProviderBadge)
>
> 1.0.10+48 거부 → +59 까지 누적 19가지 강화 + 부가 기능 다수 적용

---

## 1. App Store Connect 메시지 답변 (영문, Resolution Center 입력용 — 4000자 이내)

```
Hello App Review Team,

Thank you for the continued review. Build 1.0.10 (59) addresses every
concern raised across the prior rounds.

AGE RATING ADJUSTED TO 16+

After reviewing Apple's guidance and our own UGC analysis, we have
adjusted the app's age rating to 16+ via the IARC questionnaire. We
believe 16+ — combined with our human student-ID verification — is
the appropriate rating for an app whose entire user base consists of
verified high-school students. The previous 12+ rating did not fully
reflect the nature of social interaction in the app; 16+ does.

NO ANONYMOUS POSTING — STRONGER THAN EVER IN THIS BUILD

Every Claspeek account is verified by our staff via student-ID photo
review (1–3 business days). There is no guest mode, no anonymous
posting, and no way to bypass verification. Posts and comments now
surface the author's identity in MULTIPLE places:

  • Composer: a banner shows the verified school, grade, and
    nickname with the notice "학생증 인증된 본인 정보가 게시글에
    함께 공개됩니다" (your verified student-ID identity is published).
  • Feed cards & detail screens: the author's nickname is shown
    together with a unique account code (e.g., "minji #A7K2"), so a
    single person cannot appear under different identities.
  • Feed cards: an AuthorProviderBadge shows the author's login
    email and the OAuth provider logo (Google / Kakao / Naver /
    Apple), making the identity source explicit at a glance.

A reviewer cannot reasonably interpret any post as "anonymous."

SERVER-SIDE IMMEDIATE REMOVAL FROM THE FEED

When a user reports a post / pledge / vote / comment, the server
itself excludes that content from every subsequent feed response sent
to the reporter — across community, vote, pledge, trending, search,
ranking, my-posts, my-comments, liked, and saved (10 feed providers).
The reporter will not see it again on this device, on a different
device, after reinstall, or after refresh. Direct URL / deep link
access also returns NOT_FOUND.

AUTO-HIDE + RESOLUTION NOTIFICATION

  • Auto-hide: 3 reports on the same content triggers immediate
    server-side hide for every user, without waiting for staff.
  • Resolution: when staff resolves a report (HIDDEN / BANNED /
    NO_ACTION / DISMISSED), the reporter receives a push notification.

REPORTING & POST/COMMENT-LEVEL ACTIONS

  • Every post detail shows a flag icon directly on the action bar
    (non-owner) — one tap to report.
  • Every comment / reply has a ⋮ menu: owner gets "Delete comment",
    non-owner gets "Report comment" (8 categories, 24h SLA in-sheet).
  • Block: one-tap from any post; managed at Settings → Privacy &
    Security → Blocked Users.

ALL FOUR GUIDELINE 1.2 SAFEGUARDS

  • Content filter — server-side 3-tier (HIGH / MEDIUM / LOW) at
    submission time
  • Reporting — as above
  • Blocking — as above
  • EULA with zero-tolerance clause (Article 5-2): mandatory at
    signup; always at Settings → App Info and
    https://www.claspeek.com/terms/

Developer contact is shown at Settings → App Info; an in-app
Customer Support form is at Settings → Customer Support. iOS Privacy
Manifest (PrivacyInfo.xcprivacy) is included, with all data
collection categories declared as Tracking=false.

REQUEST

Given (a) the rating is now 16+, (b) every user is human-verified
with their school/grade/nickname/code/email/provider visible on every
post, and (c) all UGC safeguards are implemented and surfaced, we
believe the app now fully aligns with Guideline 1.2.

A pre-verified demo account is provided in App Review Information.
We are happy to demonstrate the verification flow and safeguards live
at a Meet with Apple appointment if helpful.

Thank you.

Sincerely,
Claspeek Team
```

> **글자 수**: 약 3,400자 (4000자 한도 안에 약 600자 여유)

---

## 2. App Store Connect → 앱 심사 정보 → 메모 (Reviewer Notes, 4000자 이내 압축본)

```
=== ABOUT ===
Claspeek is a community + planner app exclusively for VERIFIED Korean
high-school students (target age 16–18).

=== DEMO ACCOUNT ===
The provided demo account has ALREADY passed our manual student-ID
verification. Upon login the reviewer can immediately: browse feeds,
post / comment, report any post / comment / vote / pledge, delete own
posts / comments, block users (Settings → Privacy & Security →
Blocked Users), view EULA (Settings → App Info), contact us
(claspeek.official@gmail.com).

=== NO ANONYMOUS POSTING — BY DESIGN ===
New signups must: (1) agree to Terms/EULA (zero-tolerance clause),
(2) submit a Korean student ID photo, (3) wait 1–3 business days for
HUMAN review by staff, (4) only then sign in / post. There is no guest
mode, no anonymous mode, no way to bypass. Reviewers attempting signup
will hit "Verification Pending" — by design.

=== AUTHOR IDENTITY ON EVERY POST (NOT ANONYMOUS) ===
On every feed card and detail screen, the author is shown with:
  • verified school + grade (e.g., "Seoul HS · 2학년")
  • nickname + unique account code (e.g., "minji #A7K2") — a single
    person cannot appear under different identities
  • AuthorProviderBadge: login email + OAuth provider logo
    (Google / Kakao / Naver / Apple)
A reviewer cannot reasonably interpret any post as anonymous.

=== 5 REVIEW SCENARIOS ===
1) Report a post → flag icon on action bar (or ⋮ → Report) → choose
   reason → submit. Sheet closes, toast: "신고가 접수되었습니다. 이
   콘텐츠는 더 이상 표시되지 않으며, 24시간 이내에 검토됩니다."
   Pull-to-refresh: reported post is GONE — stays gone across refresh,
   app restart, reinstall, and direct deep-link entry (NOT_FOUND).
2) Delete your own post → ⋮ → Delete → confirm → instantly gone.
3) Report a comment → ⋮ on comment → "Report comment" → submit →
   refresh → comment is GONE.
4) Delete your own comment → ⋮ → Delete → instantly gone.
5) Block a user → ⋮ → Block → confirm → all their posts/comments
   disappear from every feed. Manage at Settings → Privacy & Security
   → Blocked Users.

=== UGC SAFEGUARDS (1.2) ===
• Content filter: server-side 3-tier (HIGH/MEDIUM/LOW) blocks
  profanity / hate / sexual / violent content at submission time.
• Reporting: Report action on every post / comment / reply,
  8 categories (Spam, Harassment, Hate Speech, Sexual Content,
  Violence, Illegal, Impersonation, Other), 24h SLA disclosed in-sheet.
• Auto-hide: 3 reports on the same content → automatically hidden
  from every feed for everyone, without waiting for staff review.
• Server-side immediate removal: reported content is excluded from
  every feed response (10 feed providers) sent to the reporter, on
  any device, after restart/reinstall. Direct URL is also blocked.
• Resolution notification: when staff resolves a report, the reporter
  receives a push notification.
• Blocking: one-tap, managed at Settings → Privacy & Security →
  Blocked Users.
• EULA with zero-tolerance clause (Article 5-2): mandatory at signup;
  always at Settings → App Info and https://www.claspeek.com/terms/.
• Compose-screen identity card: every composer prominently shows the
  author's verified school, grade, nickname — anonymity is impossible
  by design.

=== AGE RATING ===
The app's age rating has been adjusted to 16+ via the IARC
questionnaire. Combined with our human student-ID verification, 16+
is the appropriate rating for our verified high-school audience.

=== CONTACT ===
Use the email/phone in the contact info fields. We respond within
24 hours on business days. Thank you.
```

> **글자 수**: 약 3,050자 (4000자 제한 안전 마진 약 950자)

---

## 3. 한국어 답변 (Apple 한국 검토팀이 본다면)

```
안녕하세요, App Review 팀.

검토에 감사드립니다. 1.0.10 (59) 빌드는 그동안 지적해 주신 모든
사항을 반영했습니다.

[연령 등급 16+ 로 조정]

IARC 설문을 통해 앱의 연령 등급을 16+ 로 조정했습니다. 인증된
고등학생만 이용하는 앱이라 하더라도, 사용자 간 상호작용의 성격을
고려하면 12+ 보다 16+ 가 더 적절한 등급이라 판단했습니다. 학생증
사람 검수 인증과 결합되어 안전성이 확보됩니다.

[익명 게시 불가 — 이번 빌드에서 더 강화]

모든 Claspeek 계정은 운영팀이 학생증 사진을 직접 검토하여 승인
(1~3 영업일). 익명 모드, 우회 가입 모두 불가능합니다. 게시글과
댓글에는 작성자 신원이 여러 곳에서 명시됩니다:

  • 작성 화면 상단: 학교 · 학년 · 닉네임 + "학생증 인증된 본인
    정보가 게시글에 함께 공개됩니다" 안내
  • 피드 카드/상세 화면: 닉네임 + 고유 계정 코드 (예: "민지 #A7K2")
    — 같은 사람이 다른 신원으로 가장 불가능
  • 피드 카드: AuthorProviderBadge — 로그인 이메일 + OAuth provider
    로고 (Google / Kakao / Naver / Apple)

[서버 측 자동 제거]

사용자가 게시글/다짐/투표/댓글을 신고하면, 서버가 해당 콘텐츠를
신고자에게 응답하는 모든 피드에서 직접 제외 (10개 피드 provider).
같은 디바이스, 다른 디바이스, 재설치, 직접 URL/딥링크 접근 모두
차단 (NOT_FOUND).

[자동 hide + 처리 결과 알림]

  • 같은 콘텐츠 3건 신고 → 운영팀 대기 없이 즉시 자동 hide
  • 운영팀 처리 시 신고자에게 결과 푸시 알림
    (HIDDEN / BANNED / NO_ACTION / DISMISSED)

[신고/차단/필터/EULA]

  • 신고: 모든 게시글/댓글/답글, 8 카테고리, 24h SLA in-sheet 명시
  • 게시글 상세 액션바에 신고 플래그 아이콘 직접 노출 (한 번의 탭)
  • 댓글 ⋮ 메뉴: 본인 삭제, 타인 신고
  • 차단: 한 번의 탭, 설정 → 개인정보 및 보안 → 차단한 사용자
  • 콘텐츠 필터: 서버 측 3단계(HIGH/MEDIUM/LOW) 자동 차단
  • EULA: 회원가입 시 필수, 무관용 조항 (제5조의2)
  • 개발자 연락처: 설정 → 앱 정보
  • iOS Privacy Manifest (PrivacyInfo.xcprivacy) 포함,
    모든 데이터 수집 카테고리 Tracking=false

(a) 16+ 등급 조정, (b) 모든 사용자 학생증 사람 인증 + 게시글마다
학교/학년/닉네임/코드/이메일/provider 노출, (c) 모든 UGC 안전장치
구현 및 액션바 표면 노출 — 이번 빌드는 Guideline 1.2 요구를
완전히 충족합니다.

App Review Information 에 사전 인증된 데모 계정이 제공되어
있습니다. 필요 시 Meet with Apple 미팅에서 인증 절차와 안전장치를
라이브로 시연해 드릴 수 있습니다.

감사합니다.

Claspeek 팀 드림
```

---

## 4. 시연 영상 시나리오 (사용자 본인 녹화용, 30~60초)

iPad Air 11-inch (M3) 시뮬레이터 또는 iPhone 17 + QuickTime.

| 초 | 행동 | 화면 |
|---|---|---|
| 0~5 | 피드 진입 | 카드에 **닉네임 + #코드 + 이메일 + provider 로고** 노출 (anti-anonymous) |
| 5~10 | 글쓰기 화면 진입 | **신원 카드** (학교/학년/닉네임) + 정책 배너 |
| 10~17 | 뒤로 → 게시글 상세 → 액션바 🏳 → 사유 선택 → 제출 | 신고 시트 8 카테고리 + 강화된 안내 3줄 |
| 17~22 | 토스트 확인 → 뒤로 → 피드 새로고침 | **신고한 글이 없음** |
| 22~28 | 본인 글 → ⋮ → 삭제 | 확인 다이얼로그 → 삭제 → 즉시 사라짐 |
| 28~37 | 다른 글 진입 → 댓글 ⋮ → 신고 → 제출 | 댓글 신고 시트 → 댓글 사라짐 |
| 37~45 | 본인 댓글 ⋮ → 삭제 | 즉시 사라짐 |
| 45~52 | 다른 글 → ⋮ → 차단 | 모든 피드에서 그 사용자 사라짐 |
| 52~60 | 설정 → 앱 정보 | Developer Contact 표시 |

QuickTime 으로 시뮬레이터 녹화 → mp4 50MB 이내 → Drive 또는 답변 첨부.

---

## 5. App Store Connect 사전 점검 체크리스트

제출 직전 확인:

- [ ] **연령 등급 16+ 로 변경 완료** (IARC 설문 답변 갱신 + 저장)
- [ ] App Review Information → 데모 계정 ID/PW 가 학생증 인증 완료된 상태
- [ ] App Review Information → 메모란에 위 "Reviewer Notes" 텍스트 입력 (16+ 명시)
- [ ] App Review Information → 연락처 이메일이 24h 응답 가능한 주소
- [ ] 빌드 1.0.10 (59) 가 TestFlight 처리 완료 (10~30분 소요)
- [x] 백엔드 운영 서버에 신고 자동 hide / 임계값 / 처리 결과 알림 / 상세 진입 차단 / 작성자 코드·이메일·provider 노출 코드 모두 배포 완료
- [ ] 본인 디바이스(iPhone + iPad) 에서 시연 시나리오 (특히 카드에 **#코드 + 이메일 + provider 로고** 노출) 동작 확인
- [ ] (선택) 시연 영상 mp4 + 공유 가능한 링크 준비
- [ ] App Store Connect → 거부 항목 → 빌드를 1.0.10 (59) 로 변경
- [ ] Resolution Center → 위 영문 답변 메시지 전송
- [ ] "심사에 다시 제출" 클릭

---

## 6. 자주 받을 수 있는 추가 질문 / 답변

### Q. 학생증 인증을 어떻게 검증하는가?
A. 운영팀이 1~3 영업일 내 사람이 직접 검토. 학생증 사진의 학교명, 학년, 사진과 가입 정보를 비교 확인. 위조나 불일치 시 거절.

### Q. 신고된 콘텐츠는 다른 사용자에게도 보이지 않는가?
A. 신고 직후에는 신고자에게만 즉시 제외됩니다. 같은 콘텐츠가 3건 이상 신고되면 자동으로 모든 사용자에게서 hide 됩니다 (운영팀 대기 없이). 운영팀이 24시간 내 검토 후 정책 위반이면 영구 hide(`RESOLVED_HIDDEN`), 작성자는 영구 차단(`RESOLVED_BANNED`) 가능.

### Q. 어떤 콘텐츠가 자동 필터링되는가?
A. 서버 측 ContentFilterService 가 욕설, 혐오 표현, 성적 콘텐츠, 폭력 표현을 3단계(HIGH/MEDIUM/LOW)로 분류. HIGH 는 게시 시점에 즉시 차단(`CONTENT_CONTAINS_PROFANITY`), MEDIUM 은 검토 큐에 자동 등록.

### Q. 사용자 차단은 영속적인가?
A. 네. 차단된 사용자의 게시글·댓글이 모든 피드에서 영속적으로 제외됩니다. 차단 해제는 설정 → 개인정보 및 보안 → 차단한 사용자 에서 가능.

### Q. 신고 처리 결과를 사용자가 알 수 있는가?
A. 네. 운영팀이 신고를 처리하면 (`RESOLVED_HIDDEN` / `RESOLVED_BANNED` / `RESOLVED_NO_ACTION` / `DISMISSED`) 신고자에게 푸시 알림이 도착합니다.

### Q. 직접 URL이나 딥링크로 신고된 글에 접근할 수 있는가?
A. 아니요. 서버의 `getById` 단계에서 신고자 또는 차단자가 해당 콘텐츠에 접근하면 `NOT_FOUND` 응답으로 차단됩니다. 피드뿐 아니라 모든 진입 경로에서 일관되게 hide 됩니다.
