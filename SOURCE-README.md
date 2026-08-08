# Discord Server Bot Source

هذا هو سورس بوت Discord كامل بالعربي والإنجليزي.

## التشغيل

1. ثبّت Node.js 20 أو أحدث و pnpm.
2. نفّذ `pnpm install` من جذر المشروع.
3. أنشئ تطبيقاً وبوتاً من Discord Developer Portal.
4. فعّل:
   - Message Content Intent
   - Server Members Intent
   - Server Presences Intent (اختياري للألعاب/الحضور)
5. أضف البوت إلى السيرفر بصلاحيات:
   - View Channels
   - Send Messages
   - Embed Links
   - Attach Files
   - Read Message History
   - Manage Channels
   - Manage Roles
   - Manage Messages
   - Manage Members
   - Kick Members
   - Ban Members
   - Moderate Members
   - Connect و Speak لوضع 24/7
6. خزّن التوكن في متغير البيئة `DISCORD_TOKEN`. لا تضعه داخل الكود أو Git.
7. شغّل:

```bash
pnpm --filter @workspace/api-server run dev
```

## البداية داخل Discord

```text
/setup
```

يمشي الإعداد خطوة بخطوة لاختيار:

1. روم الترحيب ثم نصه وصورته/فيديوه.
2. روم التذاكر ثم نصه وصورته/فيديوه.
3. روم إشعارات المستويات ثم نصه وصورته/فيديوه.
4. روم الستريك ثم عنوانه وصورته/فيديوه.

بعدها ينشئ البوت الرتب، الأقسام، الرومات، ورومات السجلات الافتراضية.

## الأوامر المهمة

- `/bot-info` — شرح كامل للبوت.
- `/help` — الأوامر حسب الأقسام.
- `/ticket setup` — إرسال لوحة التذاكر.
- `/set` — تعديل أي روم أو نص أو صورة بعد الإعداد.
- `/game help` — الألعاب المتاحة.

## الألعاب

`coinflip`, `dice`, `rps`, `slots`, `8ball`, `math`, `trivia`,
`guess-start`, `guess`, و `blackjack`.

## الملفات الأساسية

- `src/discord/bot.ts` — أوامر Discord، الإعداد التفاعلي، الألعاب والأحداث.
- `src/discord/constants.ts` — الرتب، رتب المستويات، تخطيط الرومات والمساعدة.
- `src/discord/store.ts` — التخزين المحلي لإعدادات السيرفرات.
- `src/discord/types.ts` — أنواع الإعدادات والبيانات.

هذا الأرشيف لا يحتوي على `DISCORD_TOKEN` أو `node_modules` أو ملفات build.