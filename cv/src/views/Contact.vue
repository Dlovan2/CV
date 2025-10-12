<template>
  <div class="contact">
    <div class="contact-header">
      <h1>Get In Touch</h1>
      <p class="tagline">Let's connect and explore opportunities together</p>
    </div>

    <div class="content-wrapper">
      <section class="contact-info">
        <h2>Contact Information</h2>
        <div class="info-cards">
          <ContactCard
            icon="📱"
            title="Phone"
            :content="contactInfo.phone"
            :href="`tel:${contactInfo.phone}`"
          />

          <ContactCard
            icon="✉️"
            title="Email"
            :content="contactInfo.email"
            :href="`mailto:${contactInfo.email}`"
          />

          <ContactCard
            icon="📍"
            title="Location"
            :content="contactInfo.address"
          />
        </div>

        <div class="availability">
          <h3>Availability</h3>
          <p>I'm currently available for:</p>
          <ul>
            <li>Internship opportunities</li>
            <li>Part-time positions</li>
            <li>Freelance projects</li>
            <li>Collaboration and networking</li>
          </ul>
        </div>
      </section>
    </div>
  </div>
</template>

<script setup lang="ts">
import ContactCard from '../components/ContactCard.vue';

interface ContactInfo {
  phone: string;
  email: string;
  address: string;
}

const contactInfo: ContactInfo = {
  phone: '07503889591',
  email: 'dlovanfaisal180@gmail.com',
  address: 'Erbil, Braiaty'
};
</script>

<style scoped>
.contact {
  min-height: 100vh;
  padding-bottom: 4rem;
}

.contact-header {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 4rem 2rem;
  text-align: center;
}

.contact-header h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
  animation: fadeInUp 0.8s ease-out;
}

.tagline {
  font-size: 1.3rem;
  opacity: 0.95;
  animation: fadeInUp 0.8s ease-out 0.2s both;
}

.content-wrapper {
  max-width: 900px;
  margin: 0 auto;
  padding: 3rem 2rem;
}

.contact-info h2 {
  color: #667eea;
  font-size: 2rem;
  margin-bottom: 2rem;
  border-bottom: 3px solid #667eea;
  padding-bottom: 0.5rem;
  text-align: center;
}

.info-cards {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem;
  margin-bottom: 2rem;
}

.availability {
  background: white;
  padding: 2.5rem;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  animation: fadeInUp 0.8s ease-out 0.2s both;
  max-width: 600px;
  margin: 0 auto;
}

.availability h3 {
  color: #667eea;
  margin-bottom: 1rem;
  font-size: 1.5rem;
  text-align: center;
}

.availability p {
  color: #333;
  margin-bottom: 1rem;
  text-align: center;
  font-size: 1.1rem;
}

.availability ul {
  list-style: none;
  padding: 0;
}

.availability li {
  color: #666;
  padding: 0.75rem 0;
  padding-left: 2rem;
  position: relative;
  font-size: 1.05rem;
}

.availability li::before {
  content: '✓';
  position: absolute;
  left: 0;
  color: #667eea;
  font-weight: bold;
  font-size: 1.2rem;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  .contact-header h1 {
    font-size: 2rem;
  }

  .tagline {
    font-size: 1.1rem;
  }

  .info-cards {
    grid-template-columns: 1fr;
  }

  .availability {
    padding: 1.5rem;
  }
}
</style>
