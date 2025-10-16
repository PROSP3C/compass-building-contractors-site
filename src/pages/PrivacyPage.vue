<script lang="ts" setup>
  import ContentSection from 'src/components/ContentSection.vue'

  const sections = [
    {
      title: '',
      paragraph: `Effective Date: 16/10/2025 Last Updated: 16/10/2025 Compass Building Contractors Ltd ("we", "our", or "us") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, and safeguard your personal information when you visit our website or contact us directly.`,
    },
    {
      title: 'Information We Collect',
      paragraph: `We may collect and process the following types of personal data: Contact details: Name, email address, phone number, and postal address Project information: Details you provide when requesting quotes or services Website usage data: IP address, browser type, pages visited, and time spent on our site Communication records: Emails, messages, or calls related to enquiries or services`,
    },
    {
      title: 'How We Use Your Information',
      paragraph: `We use your personal data to: Respond to enquiries and provide quotes Deliver services and manage projects Improve our website and customer experience Comply with legal obligations and resolve disputes We do not sell or rent your personal data to third parties.`,
    },
    {
      title: 'Data Security',
      paragraph: `We take appropriate technical and organisational measures to protect your data from unauthorised access, loss, or misuse. However, no method of transmission over the internet is 100% secure.`,
    },
    {
      title: 'Cookies & Analytics',
      paragraph: `Our website may use cookies and analytics tools to enhance user experience and monitor site performance. You can manage cookie preferences through your browser settings.`,
    },
    {
      title: 'Sharing Your Data',
      paragraph: `We may share your data with trusted third-party service providers (e.g., hosting, email, accounting) who assist us in operating our business. These providers are contractually obligated to protect your data.`,
    },
    {
      title: '',
      paragraph: `We may share your data with trusted third-party service providers (e.g., hosting, email, accounting) who assist us in operating our business. These providers are contractually obligated to protect your data. 🇬🇧 Your Rights (UK GDPR) You have the right to: Access the personal data we hold about you Request correction or deletion of your data Object to or restrict certain types of processing Withdraw consent (where applicable) To exercise your rights, please contact us at compass.buildingcontractors@gmail.com.`,
    },
  ]
</script>

<template>
  <div>
    <ContentSection
      section-title="Privacy Policy"
      :sections="sections"
      :dark="false"
    />
  </div>
</template>
