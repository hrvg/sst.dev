---
layout: default
title: SST Guide
description: Learn how to build full-stack apps using serverless and React on AWS.
---

<div class="guide-page">

  <div class="title">
    <p class="eyebrow">Join readers from the biggest companies in the world</p>
    <h2>SST Guide</h2>
    <h4>
      The most widely read resource for building full-stack apps using serverless and React on AWS.
    </h4>
  </div>

  <div class="readers">
    {% include reader-logos.html %}
  </div>

  <div id="table-of-contents" class="table-of-contents">

    <div class="all-chapters">
      {% include toc-chapters.html items=site.data.chapterlist.preface id="preface" index="1" %}

      {% include toc-chapters.html items=site.data.chapterlist.intro id="intro" index="2" %}

      {% include toc-chapters.html items=site.data.chapterlist.setup-aws id="setup-aws" index="3" %}
      {% include toc-chapters.html items=site.data.chapterlist.setup-sst id="setup-sst" index="4" %}
      {% include toc-chapters.html items=site.data.chapterlist.setup-sst-backend id="setup-sst-backend" index="5" %}
      {% include toc-chapters.html items=site.data.chapterlist.build-sst-api id="build-sst-api" index="6" %}
      {% include toc-chapters.html items=site.data.chapterlist.add-auth-stack id="add-auth-stack" index="7" %}
      {% include toc-chapters.html items=site.data.chapterlist.handling-secrets id="handling-secrets" index="8" %}
      {% include toc-chapters.html items=site.data.chapterlist.unit-tests id="unit-tests" index="9" %}
      {% include toc-chapters.html items=site.data.chapterlist.cors-sst id="cors-sst" index="10" %}

      {% include toc-chapters.html items=site.data.chapterlist.setup-react id="setup-react" index="11" %}
      {% include toc-chapters.html items=site.data.chapterlist.react-routes id="react-routes" index="12" %}
      {% include toc-chapters.html items=site.data.chapterlist.setup-amplify id="setup-amplify" index="13" %}
      {% include toc-chapters.html items=site.data.chapterlist.build-react id="build-react" index="14" %}
      {% include toc-chapters.html items=site.data.chapterlist.secure-pages id="secure-pages" index="15" %}

      {% include toc-chapters.html items=site.data.chapterlist.custom-domains id="custom-domains" index="16" %}
      {% include toc-chapters.html items=site.data.chapterlist.automating-deployments id="automating-deployments" index="17" %}

      {% include toc-chapters.html items=site.data.chapterlist.conclusion id="conclusion" index="18" %}
    </div>

    <div class="standalone-newsletter-form-container">
      {% include standalone-newsletter-form.html %}
    </div>

    <div id="archives" class="header archives">
      <h3>Archives</h3>
      <p>Older sections of the guide available for reference.</p>
    </div>

    <div class="wrapper">

      <div class="col1">
        <div class="part">
          <div id="best-practices" class="header best-practices">
            <h3>Best Practices</h3>
          </div>
          <div class="chapters best-practices">
            {% include toc-chapters.html items=site.data.archiveslist.best-practices-intro id="best-practices-intro" %}
            {% include toc-chapters.html items=site.data.archiveslist.organize-serverless-apps id="organize-serverless-apps" %}
            {% include toc-chapters.html items=site.data.archiveslist.configure-environments id="configure-environments" %}
            {% include toc-chapters.html items=site.data.archiveslist.development-lifecycle id="development-lifecycle" %}
            {% include toc-chapters.html items=site.data.archiveslist.observability id="observability" %}
            {% include toc-chapters.html items=site.data.archiveslist.best-practices-conclusion id="best-practices-conclusion" %}
            <a class="expand"><span class="sst-button tertiary">Show all</span></a>
          </div>
        </div>

        <div class="part">
          <div id="serverless-framework" class="header serverless-framework">
            <h3>Serverless Framework</h3>
          </div>
          <div class="chapters serverless-framework">
            {% include toc-chapters.html items=site.data.archiveslist.setup-serverless id="setup-serverless" %}
            {% include toc-chapters.html items=site.data.archiveslist.setup-backend id="setup-backend" %}
            {% include toc-chapters.html items=site.data.archiveslist.build-api id="build-api" %}
            {% include toc-chapters.html items=site.data.archiveslist.users-auth id="users-auth" %}
            {% include toc-chapters.html items=site.data.archiveslist.third-party-apis id="third-party-apis" %}
            {% include toc-chapters.html items=site.data.archiveslist.infrastructure-as-code id="infrastructure-as-code" %}
            <a class="expand"><span class="sst-button tertiary">Show all</span></a>
          </div>
        </div>
      </div>

      <div class="col2">
        <div class="part">
          <div id="extra-credit" class="header extra-credit">
            <h3>Extra Credit</h3>
          </div>
          <div class="chapters expanded">
            {% include toc-chapters.html items=site.data.archiveslist.extra-backend id="extra-backend" %}
            {% include toc-chapters.html items=site.data.archiveslist.extra-auth id="extra-auth" %}
            {% include toc-chapters.html items=site.data.archiveslist.extra-frontend id="extra-frontend" %}
          </div>
        </div>
      </div>
    </div>

  </div>
</div>
