export default function AlWariqLibrary() { const books = [ { title: "فن الرسم الزيتي", category: "فنون", image: "https://images.unsplash.com/photo-1512820790803-83ca734da794?q=80&w=1200&auto=format&fit=crop" }, { title: "تاريخ الحضارات", category: "تاريخ", image: "https://images.unsplash.com/photo-1521587760476-6c12a4b040da?q=80&w=1200&auto=format&fit=crop" }, { title: "تعلم البرمجة", category: "تقنية", image: "https://images.unsplash.com/photo-1515879218367-8466d910aaa4?q=80&w=1200&auto=format&fit=crop" } ];

return ( <div className="min-h-screen bg-neutral-100 text-neutral-900" dir="rtl"> {/* Header */} <header className="bg-white shadow-sm sticky top-0 z-50"> <div className="max-w-7xl mx-auto px-6 py-4 flex items-center justify-between"> <h1 className="text-3xl font-bold">مكتبة الوارق</h1>

<nav className="hidden md:flex gap-6 text-lg">
        <a href="#home" className="hover:text-neutral-500">الرئيسية</a>
        <a href="#books" className="hover:text-neutral-500">الكتب</a>
        <a href="#categories" className="hover:text-neutral-500">الأقسام</a>
        <a href="#about" className="hover:text-neutral-500">من نحن</a>
        <a href="#contact" className="hover:text-neutral-500">اتصل بنا</a>
      </nav>
    </div>
  </header>

  {/* Hero */}
  <section
    id="home"
    className="relative h-[500px] flex items-center justify-center text-center overflow-hidden"
  >
    <img
      src="https://images.unsplash.com/photo-1507842217343-583bb7270b66?q=80&w=1600&auto=format&fit=crop"
      alt="library"
      className="absolute inset-0 w-full h-full object-cover"
    />

    <div className="absolute inset-0 bg-black/60"></div>

    <div className="relative z-10 px-6">
      <h2 className="text-5xl md:text-6xl font-bold text-white mb-6">
        أهلاً بك في مكتبة الوارق
      </h2>

      <p className="text-white/90 text-xl max-w-2xl mx-auto mb-8">
        اكتشف آلاف الكتب والروايات والمراجع العلمية في مكان واحد.
      </p>

      <button className="bg-white text-black px-8 py-3 rounded-2xl text-lg font-semibold shadow-lg hover:scale-105 transition">
        تصفح الكتب
      </button>
    </div>
  </section>

  {/* Categories */}
  <section id="categories" className="max-w-7xl mx-auto px-6 py-20">
    <div className="text-center mb-12">
      <h3 className="text-4xl font-bold mb-4">الأقسام</h3>
      <p className="text-neutral-600 text-lg">
        اختر القسم المناسب لاهتماماتك
      </p>
    </div>

    <div className="grid grid-cols-1 md:grid-cols-4 gap-6">
      {[
        "الروايات",
        "العلوم",
        "الفنون",
        "البرمجة",
        "التاريخ",
        "التنمية البشرية",
        "الأطفال",
        "اللغة الإنجليزية"
      ].map((item) => (
        <div
          key={item}
          className="bg-white rounded-3xl shadow-md p-8 text-center text-xl font-semibold hover:-translate-y-2 transition"
        >
          {item}
        </div>
      ))}
    </div>
  </section>

  {/* Books */}
  <section id="books" className="bg-white py-20">
    <div className="max-w-7xl mx-auto px-6">
      <div className="text-center mb-12">
        <h3 className="text-4xl font-bold mb-4">كتب مميزة</h3>
        <p className="text-neutral-600 text-lg">
          مجموعة مختارة من أفضل الكتب
        </p>
      </div>

      <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
        {books.map((book) => (
          <div
            key={book.title}
            className="bg-neutral-100 rounded-3xl overflow-hidden shadow-lg hover:scale-[1.02] transition"
          >
            <img
              src={book.image}
              alt={book.title}
              className="w-full h-72 object-cover"
            />

            <div className="p-6">
              <span className="text-sm bg-black text-white px-3 py-1 rounded-full">
                {book.category}
              </span>

              <h4 className="text-2xl font-bold mt-4 mb-2">
                {book.title}
              </h4>

              <p className="text-neutral-600 leading-7">
                كتاب مميز يحتوي على معلومات قيّمة ومفيدة للقراء.
              </p>

              <button className="mt-6 w-full bg-black text-white py-3 rounded-2xl hover:opacity-90 transition">
                عرض التفاصيل
              </button>
            </div>
          </div>
        ))}
      </div>
    </div>
  </section>

  {/* About */}
  <section id="about" className="max-w-6xl mx-auto px-6 py-20">
    <div className="bg-white rounded-[40px] shadow-lg p-10 md:p-16 text-center">
      <h3 className="text-4xl font-bold mb-6">من نحن</h3>

      <p className="text-lg text-neutral-700 leading-9 max-w-3xl mx-auto">
        مكتبة الوارق منصة إلكترونية تهدف إلى توفير الكتب والمعرفة لجميع
        القرّاء بطريقة حديثة وسهلة مع تصميم أنيق وتجربة استخدام مريحة.
      </p>
    </div>
  </section>

  {/* Contact */}
  <section id="contact" className="bg-black text-white py-20">
    <div className="max-w-4xl mx-auto px-6 text-center">
      <h3 className="text-4xl font-bold mb
