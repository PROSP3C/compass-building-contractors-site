<script lang="ts" setup>
  import ContentSection from 'src/components/ContentSection.vue'

  const sections = [
    {
      title: '',
      paragraph: `Effective Date: 16/10/2025 Last Updated: 16/10/2025 Welcome to the website of Compass Building Contractors Ltd ("we", "our", or "us"). By accessing or using this website, you agree to comply with and be bound by the following terms and conditions. If you do not agree, please refrain from using our site.`,
    },
    {
      title: 'Use of Our Website',
      paragraph: `This website is intended for general information about our services. You may browse, download, or print content for personal use only. You must not use this site for unlawful purposes or in any way that may damage, disable, or impair its functionality.`,
    },
    {
      title: 'Intellectual Property',
      paragraph: `All content on this website—including text, images, logos, and layout—is the property of Compass Building Contractors Ltd or licensed to us. You may not reproduce, distribute, or modify any content without our prior written consent.`,
    },
    {
      title: 'Contact & Enquiries',
      paragraph: `Any information submitted via contact forms or email is treated in accordance with our Privacy Policy. We aim to respond promptly, but we do not guarantee response times or service availability through the website.`,
    },
    {
      title: 'External Links',
      paragraph: `Our website may contain links to third-party websites. These are provided for convenience only. We do not endorse or accept responsibility for the content, privacy practices, or accuracy of external sites.`,
    },
    {
      title: 'Disclaimer',
      paragraph: `While we strive to keep our website accurate and up to date, we make no warranties or representations about the completeness or reliability of any content. All information is provided “as is” without any guarantees.`,
    },
    {
      title: 'Limitation of Liability',
      paragraph: `Compass Building Contractors Ltd shall not be liable for any direct, indirect, or consequential loss or damage arising from the use of this website or reliance on its content.`,
    },
    {
      title: 'Changes to These Terms',
      paragraph: `We reserve the right to update these Terms & Conditions at any time. Changes will be posted on this page, and continued use of the site implies acceptance of the updated terms.`,
    },
    {
      title: 'Governing Law',
      paragraph: `These Terms & Conditions are governed by the laws of England and Wales. Any disputes shall be subject to the exclusive jurisdiction of the courts of England and Wales.`,
    },
  ]
</script>

<template>
  <div>
    <ContentSection
      section-title="Terms Of Use"
      :sections="sections"
      :dark="false"
    />
  </div>
</template>
