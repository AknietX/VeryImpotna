<template>
  <div class="yandex-taxi-connection">
    <div class="header-gradient">
      <div class="header-content">
        <h1>Подключение к Яндекс.Такси | Доставка</h1>
        <p class="header-subtitle">Станьте партнёром официального сервиса №1 в Кыргызстане</p>
      </div>
    </div>

    <div class="partner-highlight">
      <div class="partner-card">
        <div class="partner-badge">Эксклюзивные условия</div>
        <h2 class="partner-title">EXPERT PARK — официальный партнёр</h2>
        <p class="partner-text">Работаем по всему Кыргызстану с лучшими условиями для водителей</p>
      </div>
    </div>

    <div class="benefits-section">
      <h2 class="section-title">Почему водители выбирают нас?</h2>
      <div class="benefits-grid">
        <div v-for="(benefit, index) in benefits" :key="index" class="benefit-card" :class="'benefit-' + (index + 1)">
          <div class="benefit-icon">
            <i :class="benefit.icon"></i>
          </div>
          <h3 class="benefit-title">{{ benefit.title }}</h3>
          <p class="benefit-text">{{ benefit.text }}</p>
          <div class="benefit-highlight">{{ benefit.highlight }}</div>
        </div>
      </div>
    </div>

    <div class="stats-section">
      <div class="stat-item">
        <div class="stat-number">10 000+</div>
        <div class="stat-label">довольных водителей</div>
      </div>
      <div class="stat-item">
        <div class="stat-number">24/7</div>
        <div class="stat-label">поддержка</div>
      </div>
      <div class="stat-item">
        <div class="stat-number">55 сом</div>
        <div class="stat-label">в сутки</div>
      </div>
    </div>

    <div class="certification-banner">
      <div class="certification-content">
        <i class="fas fa-award"></i>
        <div>
          <p class="certification-title">EXPERT PARK — сертифицированный партнёр</p>
          <p class="certification-subtitle">Яндекс.Такси и Яндекс.Доставка</p>
        </div>
      </div>
    </div>

    <div class="cta-section">
      <h2 class="cta-title">Готовы начать зарабатывать?</h2>
      <p class="cta-subtitle">Пригласите друга и получите бонус в размере 1000 сом!</p>
      <button class="cta-button">
        <span>Подключиться</span>
        <i class="fas fa-arrow-right"></i>
      </button>
      <div class="cta-note">Регистрируйтесь по промокоду Адыл Мамадалиев</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'YandexTaxiConnection',
  data() {
    return {
      benefits: [ // Убедитесь, что этот массив определен
        {
          icon: 'fas fa-wallet',
          title: 'Низкая комиссия',
          text: 'Самая выгодная ставка на рынке',
          highlight: '55 сом/сутки'
        },
        {
          icon: 'fas fa-hand-holding-usd',
          title: 'Быстрые выплаты',
          text: 'Вывод заработанных средств',
          highlight: 'Без комиссий'
        },
        {
          icon: 'fas fa-headset',
          title: 'Поддержка 24/7',
          text: 'Круглосуточная помощь',
          highlight: 'На связи всегда'
        },
        {
          icon: 'fas fa-map-marked-alt',
          title: 'Вся территория КР',
          text: 'Работаем по всему',
          highlight: 'Кыргызстану'
        },
        {
          icon: 'fas fa-bolt',
          title: 'Мгновенное подключение',
          text: 'Начинайте работать',
          highlight: 'Уже сегодня'
        },
        {
          icon: 'fas fa-shield-alt',
          title: 'Официальный партнёр',
          text: 'Гарантия надежности',
          highlight: 'Сертифицировано'
        }
      ]
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&family=Montserrat:wght@600;700&display=swap');
@import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css');

.yandex-taxi-connection {
  font-family: 'Roboto', sans-serif;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px 60px;
  color: #2c3e50;
  background-color: #f9f9f9;
}

.header-gradient {
  background: linear-gradient(135deg, #FFCC00 0%, #FF8000 100%);
  color: white;
  padding: 50px 20px;
  margin: 0 -20px 40px;
  text-align: center;
  border-radius: 0 0 30px 30px;
  box-shadow: 0 10px 30px rgba(255, 153, 0, 0.3);
  position: relative;
  overflow: hidden;
}

.header-gradient::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path fill="rgba(255,255,255,0.05)" d="M0,0 L100,0 L100,100 L0,100 Z" /></svg>');
  opacity: 0.3;
}

.header-content {
  position: relative;
  z-index: 1;
  max-width: 800px;
  margin: 0 auto;
}

h1 {
  font-family: 'Montserrat', sans-serif;
  font-weight: 700;
  font-size: 1rem;
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.2);
  margin-bottom: 15px;
  animation: fadeInDown 0.8s ease;
}

.header-subtitle {
  font-size: 1.3rem;
  font-weight: 300;
  opacity: 0.9;
  margin-bottom: 0;
}

.partner-highlight {
  max-width: 900px;
  margin: 0 auto 50px;
}

.partner-card {
  background: white;
  border-radius: 20px;
  padding: 40px 30px 30px;
  text-align: center;
  position: relative;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
  transition: transform 0.4s ease, box-shadow 0.4s ease;
  border: 1px solid rgba(255, 204, 0, 0.3);
}

.partner-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
}

.partner-badge {
  position: absolute;
  top: -15px;
  left: 50%;
  transform: translateX(-50%);
  background: #FF3333;
  color: white;
  padding: 8px 25px;
  border-radius: 25px;
  font-weight: 600;
  font-size: 0.9rem;
  box-shadow: 0 5px 15px rgba(255, 51, 51, 0.3);
  text-transform: uppercase;
  letter-spacing: 1px;
}

.partner-title {
  font-family: 'Montserrat', sans-serif;
  font-size: 1.8rem;
  color: #FF8000;
  margin-bottom: 10px;
}

.partner-text {
  font-size: 1.2rem;
  color: #555;
  margin: 0;
}

.benefits-section {
  margin: 60px 0;
}

.section-title {
  text-align: center;
  font-family: 'Montserrat', sans-serif;
  font-size: 2rem;
  color: #333;
  margin-bottom: 40px;
  position: relative;
}

.section-title::after {
  content: '';
  display: block;
  width: 80px;
  height: 4px;
  background: linear-gradient(to right, #FFCC00, #FF8000);
  margin: 15px auto 0;
  border-radius: 2px;
}

.benefits-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
  max-width: 1100px;
  margin: 0 auto;
}

.benefit-card {
  background: white;
  border-radius: 15px;
  padding: 30px 25px;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.05);
  transition: all 0.4s ease;
  position: relative;
  overflow: hidden;
  text-align: center;
  border-top: 5px solid;
}

.benefit-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.1);
}

.benefit-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 5px;
  background: linear-gradient(to right, #FFCC00, #FF8000);
}

.benefit-1 { border-color: #4CAF50; }
.benefit-2 { border-color: #2196F3; }
.benefit-3 { border-color: #9C27B0; }
.benefit-4 { border-color: #FF9800; }
.benefit-5 { border-color: #E91E63; }
.benefit-6 { border-color: #00BCD4; }

.benefit-icon {
  font-size: 2.5rem;
  color: #FF8000;
  margin-bottom: 20px;
}

.benefit-title {
  font-family: 'Montserrat', sans-serif;
  font-size: 1.4rem;
  margin-bottom: 15px;
  color: #333;
}

.benefit-text {
  color: #666;
  margin-bottom: 20px;
  font-size: 1rem;
}

.benefit-highlight {
  font-family: 'Montserrat', sans-serif;
  font-weight: 700;
  font-size: 1.3rem;
  color: #FF3333;
  background: rgba(255, 204, 0, 0.1);
  padding: 8px 15px;
  border-radius: 30px;
  display: inline-block;
}

.stats-section {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  max-width: 800px;
  margin: 60px auto;
  background: white;
  padding: 30px;
  border-radius: 15px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
}

.stat-item {
  text-align: center;
  padding: 0 20px;
  margin: 10px 0;
}

.stat-number {
  font-family: 'Montserrat', sans-serif;
  font-size: 2.5rem;
  font-weight: 700;
  color: #FF8000;
  margin-bottom: 5px;
}

.stat-label {
  font-size: 1.1rem;
  color: #555;
}

.certification-banner {
  background: linear-gradient(135deg, #4285F4 0%, #34A853 100%);
  color: white;
  padding: 30px;
  border-radius: 15px;
  margin: 60px 0;
  box-shadow: 0 10px 30px rgba(66, 133, 244, 0.3);
  position: relative;
  overflow: hidden;
}

.certification-banner::before {
  content: '';
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0) 70%);
  transform: rotate(30deg);
}

.certification-content {
  display: flex;
  align-items: center;
  justify-content: center;
  max-width: 800px;
  margin: 0 auto;
  position: relative;
  z-index: 1;
}

.certification-content i {
  font-size: 3rem;
  margin-right: 25px;
  color: #FFCC00;
}

.certification-title {
  font-family: 'Montserrat', sans-serif;
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 5px;
}

.certification-subtitle {
  font-size: 1.2rem;
  opacity: 0.9;
  margin: 0;
}

.cta-section {
  text-align: center;
  max-width: 700px;
  margin: 80px auto 0;
  padding: 40px;
  background: white;
  border-radius: 20px;
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.08);
  position: relative;
  overflow: hidden;
}

.cta-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 10px;
  background: linear-gradient(to right, #FFCC00, #FF8000);
}

.cta-title {
  font-family: 'Montserrat', sans-serif;
  font-size: 2rem;
  color: #333;
  margin-bottom: 15px;
}

.cta-subtitle {
  font-size: 1.2rem;
  color: #555;
  margin-bottom: 30px;
  max-width: 500px;
  margin-left: auto;
  margin-right: auto;
}

.cta-button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  background: linear-gradient(135deg, #FF3333 0%, #FF8000 100%);
  color: white;
  border: none;
  padding: 18px 35px;
  font-size: 1.2rem;
  font-weight: 600;
  border-radius: 50px;
  cursor: pointer;
  transition: all 0.4s ease;
  box-shadow: 0 10px 25px rgba(255, 51, 51, 0.3);
  margin-bottom: 20px;
  overflow: hidden;
  position: relative;
}

.cta-button::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, rgba(255,255,255,0.2) 0%, rgba(255,255,255,0) 100%);
  transform: translateX(-100%);
  transition: transform 0.4s ease;
}

.cta-button:hover {
  transform: translateY(-5px);
  box-shadow: 0 15px 35px rgba(255, 51, 51, 0.4);
}

.cta-button:hover::after {
  transform: translateX(0);
}

.cta-button i {
  margin-left: 10px;
  transition: transform 0.3s ease;
}

.cta-button:hover i {
  transform: translateX(5px);
}

.cta-note {
  font-size: 1rem;
  color: #FF3333;
  font-weight: 600;
}

@keyframes fadeInDown {
  from {
    opacity: 0;
    transform: translateY(-30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  h1 {
    font-size: 5rem;
  }

  .header-subtitle {
    font-size: 1.1rem;
  }

  .partner-title {
    font-size: 1.5rem;
  }

  .benefits-grid {
    grid-template-columns: 1fr;
  }

  .stats-section {
    flex-direction: column;
    align-items: center;
  }

  .stat-item {
    margin: 15px 0;
  }

  .certification-content {
    flex-direction: column;
    text-align: center;
  }

  .certification-content i {
    margin-right: 0;
    margin-bottom: 15px;
  }
}
</style>
