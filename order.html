/* ============ الحد الممتاز — منصة 2027 ============ */
document.addEventListener('DOMContentLoaded', () => {

  /* ---------- معاينة الكتاب: تقليب الصفحات ---------- */
  const pages = Array.from(document.querySelectorAll('.book-page'));
  let cur = 0; // الصفحة الحالية (0 = الأولى)

  const show = (msg) => {
    const t = document.getElementById('toast');
    if (!t) return;
    t.textContent = msg;
    t.classList.add('show');
    clearTimeout(t._h);
    t._h = setTimeout(() => t.classList.remove('show'), 2200);
  };

  const renderBook = () => {
    pages.forEach((p, i) => {
      // الصفحات اللي فاتت تترمي ورا
      p.classList.toggle('flipped', i < cur);
      p.style.zIndex = (i < cur) ? 0 : (pages.length - i);
    });
  };

  const next = document.getElementById('nextPage');
  const prev = document.getElementById('prevPage');
  if (next && prev && pages.length) {
    next.addEventListener('click', () => {
      if (cur < pages.length - 1) { cur++; renderBook(); }
      else show('ده كان عرض مجاني — الكتاب الكامل على منصة 2027 📚');
    });
    prev.addEventListener('click', () => {
      if (cur > 0) { cur--; renderBook(); }
    });
    // قلب بالسحب/السكرول؟ نكتفي بالأزرار عشان الخفة
  }

  /* ---------- صفحة الطلب ---------- */
  // تفعيل ستايل المواد المختارة
  document.querySelectorAll('.subj input').forEach(cb => {
    const paint = () => cb.closest('.subj').classList.toggle('on', cb.checked);
    cb.addEventListener('change', paint); paint();
  });

  // حساب تقديري لسعر التكلفة
  const COST_PER_SUBJECT = 55;   // تقدير للورق+الطباعة لكل مادة
  const DELIVERY_BASE = 45;      // تقدير أساسي للتوصيل
  const subjectsBox = document.getElementById('subjects');
  const priceVal = document.getElementById('priceVal');
  const updatePrice = () => {
    if (!subjectsBox || !priceVal) return;
    const n = subjectsBox.querySelectorAll('input:checked').length;
    if (n === 0) { priceVal.textContent = '—'; return; }
    const total = n * COST_PER_SUBJECT + DELIVERY_BASE;
    priceVal.textContent = `≈ ${total} جنيه (${n} ${n > 1 ? 'مواد' : 'مادة'} + توصيل)`;
  };
  if (subjectsBox) {
    subjectsBox.addEventListener('change', updatePrice);
  }

  // أرقام الواتساب — عدّل الرقمين من هنا بس
  const WA_BOYS  = '201101258549';
  const WA_GIRLS = '201101258549'; // TODO: ضع رقم الطالبات المصممات

  const buildMsg = (who) => {
    const name = (document.getElementById('name')?.value || '').trim();
    const gov  = (document.getElementById('gov')?.value || '').trim();
    const subs = Array.from(document.querySelectorAll('#subjects input:checked')).map(c => c.value);
    let m = `السلام عليكم 👋 أنا ${who === 'girls' ? 'طالبة' : 'طالب'} وعايز أطلب كتاب الحد الممتاز 📚`;
    if (name) m += `\nالاسم: ${name}`;
    if (gov)  m += `\nالمحافظة: ${gov}`;
    if (subs.length) m += `\nالمواد: ${subs.join('، ')}`;
    if (priceVal && priceVal.textContent !== '—') m += `\nالتكلفة التقديرية: ${priceVal.textContent}`;
    const notes = (document.getElementById('notes')?.value || '').trim();
    if (notes) m += `\nملاحظات: ${notes}`;
    return encodeURIComponent(m);
  };

  const openWA = (num, who) => {
    window.open(`https://wa.me/${num}?text=${buildMsg(who)}`, '_blank');
  };
  document.getElementById('waBoys')?.addEventListener('click', () => openWA(WA_BOYS, 'boys'));
  document.getElementById('waGirls')?.addEventListener('click', () => openWA(WA_GIRLS, 'girls'));

  // إرسال الاستمارة → يفتح واتساب برسالة جاهزة
  document.getElementById('orderForm')?.addEventListener('submit', (e) => {
    e.preventDefault();
    const phone = (document.getElementById('phone')?.value || '').replace(/\D/g, '');
    if (phone.length < 10) { show('اتأكد من رقم التليفون الأول 🙏'); return; }
    const subs = document.querySelectorAll('#subjects input:checked').length;
    if (subs === 0) { show('اختار مادة واحدة على الأقل 📚'); return; }
    show('تمام! بيتم تحويلك لواتساب لتأكيد طلبك 🚀');
    setTimeout(() => openWA(WA_BOYS, 'boys'), 800);
  });
});
