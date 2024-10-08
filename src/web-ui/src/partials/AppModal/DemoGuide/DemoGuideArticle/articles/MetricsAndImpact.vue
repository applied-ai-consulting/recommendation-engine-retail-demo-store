<template>
  <ArticleLayout>
    <template #heading>Metrics and understanding impact</template>

    <p>
      You can measure the performance of ML recommender systems using offline and online metrics.
    </p>

    <p>
      Online metrics are the empirical results observed in your user’s interactions with real-time recommendations
      provided in a live environment.
    </p>

    <p>
      Offline metrics allow you to view the effects of modifying hyperparameters and algorithms used to train your
      models, calculated against historical data.
    </p>

    <p class="offline-metrics">
      Amazon Personalize generates offline metrics using test datasets derived from the historical data you provide.
      These metrics showcase how the model recommendations performed against historical data. Offline metrics are a
      great representation of how your hyperparameters and data features influence your model’s performance against
      historical data. To find empirical evidence of the impact of Amazon Personalize recommendations on your business
      metrics, such as click-through rate, conversion rate, or revenue, you should test these recommendations in a live
      environment, getting them in front of your customers.
    </p>

    <ArticleFeature class="mb-5">
      <template #title>AWS Machine Learning Blog</template>

      <template #default>
        <h1 class="blog-post-title mb-0">
          <a
            href="https://aws.amazon.com/blogs/machine-learning/using-a-b-testing-to-measure-the-efficacy-of-recommendations-generated-by-amazon-personalize/"
            target="_blank"
            rel="noreferrer noopener"
            >Using A/B testing to measure the efficacy of recommendations generated by Amazon Personalize</a
          >
        </h1>
        <div class="author mb-2">by Luis Lopez Soria | on <time>20 AUG 2020</time></div>

        <Quote>
          <template #quote>
            Machine learning (ML)-based recommender systems aren’t a new concept, but developing such a system can be a
            resource-intensive task—from data management during training and inference, to managing scalable real-time
            ML-based API endpoints. Amazon Personalize allows you to easily add sophisticated personalization
            capabilities to your applications by using the same ML technology used on Amazon.com for…
          </template>
          <template #default
            ><a
              href="https://aws.amazon.com/blogs/machine-learning/using-a-b-testing-to-measure-the-efficacy-of-recommendations-generated-by-amazon-personalize/"
              target="_blank"
              rel="noreferrer noopener"
              >Read more</a
            ></template
          >
        </Quote>

        <div class="mt-2"><img src="/personalize-ab-testing.png" alt="AB Testing" class="img-fluid" /></div>
      </template>
    </ArticleFeature>

    <ArticleFeature class="my-5">
      <template #title>AWS Partner Network (APN) Blog</template>

      <template #default>
        <div :class="{ 'apn-container': true, 'apn-container--mobile': isMobile }">
          <div class="apn-amplitude">
            <img src="/amplitude.jpg" alt="" class="img-fluid" />
          </div>

          <div class="apn-badge">
            <img src="/apn-badge.jpg" alt="" class="img-fluid" />
          </div>

          <div class="apn-title">
            <h1 class="blog-post-title mb-0">
              <a
                href="https://aws.amazon.com/blogs/machine-learning/using-a-b-testing-to-measure-the-efficacy-of-recommendations-generated-by-amazon-personalize/"
                target="_blank"
                rel="noreferrer noopener"
                >Measuring the Effectiveness of Personalization with Amplitude and Amazon Personalize</a
              >
            </h1>
            <div class="author mb-2">by Igor Krtolica | on <time>18 AUG 2020</time></div>
          </div>

          <Quote class="apn-quote">
            <!-- <template #quote>
              <p>
                This post will present an architecture that combines Amazon Personalize and Amplitude’s product
                intelligence platform to track user behavior in real time.
              </p>
              <p>
                It’ll also show how to deploy a sample e-commerce application in your Amazon Web Services (AWS) account,
                which includes a self-guided workshop created by Amplitude to help you become familiar with its
                capabilities...
              </p>
            </template> -->
            <template #default
              ><a
                href="https://aws.amazon.com/blogs/apn/measuring-the-effectiveness-of-personalization-with-amplitude-and-amazon-personalize/"
                target="_blank"
                rel="noreferrer noopener"
                >Read more</a
              ></template
            >
          </Quote>
        </div>
      </template>
    </ArticleFeature>
  </ArticleLayout>
</template>

<script>
import { mapState } from 'vuex';

import ArticleLayout from '../ArticleLayout.vue';
import ArticleFeature from '../ArticleFeature/ArticleFeature.vue';
import Quote from '../Quote/Quote.vue';

export default {
  name: 'MetricsAndImpact',
  components: { ArticleLayout, ArticleFeature, Quote },
  computed: { ...mapState({ isMobile: (state) => state.modal.isMobile }) },
};
</script>

<style scoped>
.offline-metrics {
  margin-bottom: 9rem;
}

.blog-post-title {
  font-size: 1rem;
}

.author {
  font-size: 0.8rem;
}

.apn-container {
  display: grid;
  grid-template-columns: 200px 1fr;
  grid-gap: 20px;
  grid-template-areas:
    'Amplitude Title'
    'Badge Quote';
}

.apn-amplitude {
  grid-area: Amplitude;
}

.apn-badge {
  grid-area: Badge;
}

.apn-title {
  grid-area: Title;
}

.apn-quote {
  grid-area: Quote;
  align-self: start;
}

.apn-container--mobile {
  display: block;
}

.apn-container--mobile .apn-amplitude,
.apn-container--mobile .apn-title {
  margin-bottom: 20px;
}

.apn-container--mobile .apn-badge {
  display: none;
}
</style>
