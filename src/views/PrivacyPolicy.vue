<template>
  <div class="privacy-page">
    <!-- Navigation -->
    <nav class="navbar" :class="{ 'scrolled': isScrolled }">
      <div class="container">
        <div class="nav-content">
          <div class="logo" @click="goHome">
            <img src="/logo.png" alt="ReptilesHub" class="logo-image">
            <span class="logo-text">ReptilesHub</span>
          </div>
          <div class="nav-actions">
            <a href="https://apps.apple.com/ru/app/reptiles-hub/id6753651952" target="_blank" class="btn-primary">Скачать в App Store</a>
          </div>
        </div>
      </div>
    </nav>

    <!-- Privacy Policy Content -->
    <section class="privacy-hero">
      <div class="container">
        <h1 class="privacy-hero-title">Политика конфиденциальности</h1>
        <p class="privacy-hero-subtitle">Дата вступления в силу: 5 октября 2025 г.</p>
      </div>
    </section>

    <section class="privacy-content-section">
      <div class="container">
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

        <!-- Back to Home Button -->
        <div class="privacy-actions">
          <button @click="goHome" class="btn-back">
            <span class="btn-icon">←</span> Вернуться на главную
          </button>
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
import { useRouter } from 'vue-router'

export default {
  name: 'PrivacyPolicy',
  setup() {
    const router = useRouter()
    const isScrolled = ref(false)

    const handleScroll = () => {
      isScrolled.value = window.scrollY > 50
    }

    const goHome = () => {
      router.push('/')
    }

    onMounted(() => {
      window.addEventListener('scroll', handleScroll)
    })

    onUnmounted(() => {
      window.removeEventListener('scroll', handleScroll)
    })

    return {
      isScrolled,
      goHome
    }
  }
}
</script>

<style scoped>
.privacy-page {
  min-height: 100vh;
  background: var(--dark-bg);
}

.privacy-hero {
  padding: 120px 0 80px;
  background: linear-gradient(135deg, var(--dark-bg) 0%, var(--dark-surface) 100%);
  text-align: center;
}

.privacy-hero-title {
  font-size: 48px;
  font-weight: 800;
  margin-bottom: 16px;
  background: var(--gradient-1);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.privacy-hero-subtitle {
  font-size: 20px;
  color: var(--text-secondary);
}

.privacy-content-section {
  padding: 80px 0;
}

.privacy-content {
  max-width: 900px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.privacy-card {
  background: var(--dark-surface);
  border: 1px solid var(--dark-surface-light);
  border-radius: 16px;
  padding: 32px;
  transition: all 0.3s ease;
}

.privacy-card:hover {
  border-color: var(--primary-color);
  box-shadow: var(--shadow-lg);
}

.privacy-card-title {
  font-size: 22px;
  font-weight: 700;
  color: var(--text-primary);
  margin-bottom: 16px;
}

.privacy-text {
  font-size: 16px;
  color: var(--text-secondary);
  line-height: 1.8;
  margin-bottom: 12px;
}

.privacy-text:last-child {
  margin-bottom: 0;
}

.privacy-link {
  color: var(--secondary-color);
  text-decoration: none;
  transition: color 0.3s ease;
}

.privacy-link:hover {
  color: var(--primary-color);
  text-decoration: underline;
}

.privacy-actions {
  text-align: center;
  margin-top: 60px;
}

.btn-back {
  background: var(--gradient-1);
  color: white;
  border: none;
  padding: 16px 32px;
  font-size: 18px;
  font-weight: 600;
  border-radius: 12px;
  cursor: pointer;
  transition: all 0.3s ease;
  display: inline-flex;
  align-items: center;
  gap: 8px;
}

.btn-back:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-xl);
}

.btn-icon {
  font-size: 20px;
}

/* Mobile Responsive */
@media (max-width: 768px) {
  .privacy-hero-title {
    font-size: 36px;
  }
  
  .privacy-hero-subtitle {
    font-size: 18px;
  }
  
  .privacy-card {
    padding: 24px;
  }
  
  .privacy-card-title {
    font-size: 20px;
  }
  
  .privacy-text {
    font-size: 15px;
  }
  
  .btn-back {
    width: 100%;
    justify-content: center;
  }
}
</style>
