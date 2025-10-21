<template>
  <div class="landing">
    <!-- Navigation -->
    <nav class="navbar" :class="{ 'scrolled': isScrolled }">
      <div class="container">
        <div class="nav-content">
          <div class="logo">
            <img src="/logo.png" alt="ReptilesHub" class="logo-image">
            <span class="logo-text">ReptilesHub</span>
          </div>
          <ul class="nav-links">
            <li><a href="#features" @click="scrollTo('features')">Возможности</a></li>
            <li><a href="#about" @click="scrollTo('about')">О приложении</a></li>
            <li><a href="#privacy" @click="scrollTo('privacy')">Конфиденциальность</a></li>
            <li><a href="#contact" @click="scrollTo('contact')">Контакты</a></li>
          </ul>
          <a href="https://apps.apple.com/ru/app/reptiles-hub/id6753651952" target="_blank" class="btn-primary">Скачать в App Store</a>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
      <div class="hero-background"></div>
      <div class="container">
        <div class="hero-content">
          <div class="hero-logo-container">
            <img src="/logo.png" alt="ReptilesHub" class="hero-logo">
          </div>
          <h1 class="hero-title">
            <span class="gradient-text">Reptiles Hub</span>
            <br>Умный органайзер для рептилий
          </h1>
          <p class="hero-subtitle">
            Приложение для владельцев рептилий, амфибий и других экзотических питомцев. 
            Ведите историю каждого животного, отмечайте кормления, линьки, кладки и замеры. 
            Устанавливайте напоминания и следите за периодами карантина.
          </p>
          <div class="hero-buttons">
            <a href="https://apps.apple.com/ru/app/reptiles-hub/id6753651952" target="_blank" class="btn-hero btn-hero-primary">
              <span class="btn-icon">📱</span> Скачать для iOS
            </a>
            <button class="btn-hero btn-hero-secondary" @click="scrollTo('features')">Узнать больше</button>
          </div>
        </div>
        <div class="hero-image">
          <div class="floating-card card-1">
            <span class="card-icon">🦎</span>
            <div class="card-text">
              <div class="card-title">Карточки животных</div>
              <div class="card-subtitle">Вся информация в одном месте</div>
            </div>
          </div>
          <div class="floating-card card-2">
            <span class="card-icon">⏰</span>
            <div class="card-text">
              <div class="card-title">Напоминания</div>
              <div class="card-subtitle">Не пропустите кормление</div>
            </div>
          </div>
          <div class="floating-card card-3">
            <span class="card-icon">⭐</span>
            <div class="card-text">
              <div class="card-title">5.0 рейтинг</div>
              <div class="card-subtitle">24 отзыва в App Store</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="features">
      <div class="container">
        <h2 class="section-title">Возможности приложения</h2>
        <p class="section-subtitle">Всё необходимое для ухода за вашими питомцами</p>
        <div class="features-grid">
          <div class="feature-card" v-for="(feature, index) in features" :key="index">
            <div class="feature-icon">{{ feature.icon }}</div>
            <h3 class="feature-title">{{ feature.title }}</h3>
            <p class="feature-description">{{ feature.description }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
      <div class="container">
        <div class="about-content">
          <div class="about-image">
            <div class="about-image-placeholder">
              <span class="placeholder-icon">🦎</span>
            </div>
          </div>
          <div class="about-text">
            <h2 class="section-title">О Reptiles Hub</h2>
            <p class="about-paragraph">
              Reptiles Hub — умный органайзер для рептилий, амфибий и других экзотических питомцев. 
              Приложение создано, чтобы упростить уход и учёт событий вашей коллекции. Ведите историю 
              каждого животного, отмечайте кормления, линьки, кладки и замеры.
            </p>
            <p class="about-paragraph">
              Устанавливайте напоминания, следите за периодами карантина и добавляйте важные заметки. 
              Reptiles Hub помогает держать под контролем всё, что важно для здоровья и содержания 
              ваших питомцев.
            </p>
            <div class="about-stats">
              <div class="stat">
                <div class="stat-number">5.0</div>
                <div class="stat-label">Рейтинг App Store</div>
              </div>
              <div class="stat">
                <div class="stat-number">24</div>
                <div class="stat-label">Отзыва</div>
              </div>
              <div class="stat">
                <div class="stat-number">🍎</div>
                <div class="stat-label">iOS 18+</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Privacy Policy Section -->
    <section id="privacy" class="privacy">
      <div class="container">
        <h2 class="section-title">Политика конфиденциальности</h2>
        <p class="section-subtitle">Дата вступления в силу: 5 октября 2025 г.</p>
        
        <div class="privacy-content">
          <div class="privacy-card">
            <h3 class="privacy-card-title">1. Общие положения</h3>
            <p class="privacy-text">
              Настоящая Политика конфиденциальности определяет порядок обработки и защиты информации 
              о пользователях мобильного приложения <strong>Reptiles Hub</strong>, предоставляемого разработчиком.
            </p>
            <p class="privacy-text">
              Используя Приложение, Пользователь выражает согласие с условиями настоящей Политики. 
              Если Пользователь не согласен с условиями Политики, ему следует воздержаться от использования Приложения.
            </p>
          </div>

          <div class="privacy-card">
            <h3 class="privacy-card-title">2. Сбор и использование данных</h3>
            <p class="privacy-text">
              Приложение <strong>Reptiles Hub не собирает, не обрабатывает и не передает какие-либо персональные данные пользователей.</strong>
            </p>
            <p class="privacy-text">
              Приложение функционирует полностью <strong>в офлайн-режиме</strong> и хранит все пользовательские 
              заметки и данные <strong>локально на устройстве</strong> пользователя.
            </p>
          </div>

          <div class="privacy-card">
            <h3 class="privacy-card-title">3. Передача данных третьим лицам</h3>
            <p class="privacy-text">
              Так как Приложение не собирает данные, никакая информация не передается третьим лицам.
            </p>
            <p class="privacy-text">
              Приложение также не использует сторонние сервисы, такие как аналитика, реклама или 
              авторизация через сторонние платформы.
            </p>
          </div>

          <div class="privacy-card">
            <h3 class="privacy-card-title">4. Безопасность хранения данных</h3>
            <p class="privacy-text">
              Все данные, которые пользователь создает внутри Приложения (заметки, записи, изображения и т.д.), 
              хранятся исключительно на устройстве пользователя. Разработчик не имеет доступа к этим данным 
              и не несет ответственности за их сохранность в случае удаления Приложения или сброса устройства.
            </p>
          </div>

          <div class="privacy-card">
            <h3 class="privacy-card-title">5. Контактная информация</h3>
            <p class="privacy-text">
              По всем вопросам, связанным с использованием Приложения или настоящей Политикой конфиденциальности, 
              вы можете связаться с Разработчиком по электронной почте:<br>
              📧 <a href="mailto:pav.gre4ixin@yandex.ru" class="privacy-link">pav.gre4ixin@yandex.ru</a>
            </p>
          </div>

          <div class="privacy-card">
            <h3 class="privacy-card-title">6. Изменения Политики конфиденциальности</h3>
            <p class="privacy-text">
              Разработчик оставляет за собой право вносить изменения в настоящую Политику. 
              Новая редакция Политики вступает в силу с момента её публикации вместе с обновлением 
              Приложения или размещения на соответствующей странице в App Store.
            </p>
          </div>

          <div class="privacy-card">
            <h3 class="privacy-card-title">7. Применимое право</h3>
            <p class="privacy-text">
              Настоящая Политика регулируется законодательством <strong>Российской Федерации</strong>.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="cta">
      <div class="container">
        <div class="cta-content">
          <h2 class="cta-title">Готовы попробовать?</h2>
          <p class="cta-subtitle">
            Скачайте Reptiles Hub прямо сейчас и начните вести учёт ваших питомцев. Бесплатно!
          </p>
          <a href="https://apps.apple.com/ru/app/reptiles-hub/id6753651952" target="_blank" class="btn-cta">
            <span class="btn-icon">📱</span> Скачать в App Store
          </a>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
      <div class="container">
        <h2 class="section-title">Контакты</h2>
        <p class="section-subtitle">Есть вопросы или предложения? Свяжитесь с разработчиком</p>
        <div class="contact-content">
          <div class="contact-info">
            <div class="contact-item">
              <div class="contact-icon">📧</div>
              <div>
                <div class="contact-label">Email разработчика</div>
                <a href="mailto:pav.gre4ixin@yandex.ru" class="contact-value contact-link">pav.gre4ixin@yandex.ru</a>
              </div>
            </div>
            <div class="contact-item">
              <div class="contact-icon">👥</div>
              <div>
                <div class="contact-label">Сообщество VK</div>
                <a href="https://vk.com/reptileshub" target="_blank" class="contact-value contact-link">vk.com/reptileshub</a>
              </div>
            </div>
            <div class="contact-item">
              <div class="contact-icon">🍎</div>
              <div>
                <div class="contact-label">App Store</div>
                <a href="https://apps.apple.com/ru/app/reptiles-hub/id6753651952" target="_blank" class="contact-value contact-link">Reptiles Hub</a>
              </div>
            </div>
          </div>
          <div class="contact-message">
            <h3 class="contact-message-title">Поддержка и сообщество</h3>
            <p class="contact-message-text">
              Если у вас возникли вопросы по использованию приложения, вы нашли ошибку или 
              хотите предложить новую функцию — напишите на электронную почту или присоединяйтесь 
              к нашему сообществу ВКонтакте.
            </p>
            <p class="contact-message-text">
              В группе VK вы можете делиться опытом с другими киперами, задавать вопросы и 
              следить за обновлениями приложения. Приложение разрабатывается независимым 
              разработчиком с заботой о вашем удобстве.
            </p>
            <div class="contact-buttons">
              <a href="mailto:pav.gre4ixin@yandex.ru" class="btn-contact">
                <span class="btn-icon">✉️</span> Написать разработчику
              </a>
              <a href="https://vk.com/reptileshub" target="_blank" class="btn-contact btn-contact-secondary">
                <span class="btn-icon">👥</span> Присоединиться к VK
              </a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
      <div class="container">
        <div class="footer-content">
          <div class="footer-logo">
            <img src="/logo.png" alt="ReptilesHub" class="footer-logo-image">
            <span class="logo-text">ReptilesHub</span>
          </div>
          <p class="footer-text">© 2025 ReptilesHub. Все права защищены.</p>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import { ref, onMounted, onUnmounted } from 'vue'

export default {
  name: 'App',
  setup() {
    const isScrolled = ref(false)
    const form = ref({
      name: '',
      email: '',
      message: ''
    })

    const features = [
      {
        icon: '🦎',
        title: 'Электронные карточки',
        description: 'Создавайте карточки для каждого животного с фотографиями, морфом, полом и другими данными'
      },
      {
        icon: '📊',
        title: 'Учёт событий',
        description: 'Отмечайте кормления, линьки, кладки, замеры и ведите полную историю ваших питомцев'
      },
      {
        icon: '⏰',
        title: 'Таймеры и напоминания',
        description: 'Устанавливайте напоминания о кормлении, карантине и других важных событиях'
      },
      {
        icon: '🔗',
        title: 'Связи между животными',
        description: 'Указывайте родителей, потомство и пары для учёта разведения'
      },
      {
        icon: '📝',
        title: 'Журнал и планировщик',
        description: 'Удобный журнал событий и планировщик помогут не забыть ничего важного'
      },
      {
        icon: '📂',
        title: 'Группировка и архив',
        description: 'Организуйте коллекцию по группам и архивируйте проданных или умерших животных'
      }
    ]

    const handleScroll = () => {
      isScrolled.value = window.scrollY > 50
    }

    const scrollTo = (id) => {
      const element = document.getElementById(id)
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' })
      }
    }

    const handleSubmit = () => {
      alert('Спасибо за ваше сообщение! Мы свяжемся с вами в ближайшее время.')
      form.value = { name: '', email: '', message: '' }
    }

    onMounted(() => {
      window.addEventListener('scroll', handleScroll)
    })

    onUnmounted(() => {
      window.removeEventListener('scroll', handleScroll)
    })

    return {
      isScrolled,
      form,
      features,
      scrollTo,
      handleSubmit
    }
  }
}
</script>



