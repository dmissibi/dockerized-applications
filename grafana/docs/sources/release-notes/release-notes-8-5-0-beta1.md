---
hide_menu: true
title: Release notes for Grafana 8.5.0-beta1
---

<!-- Auto generated by update changelog github action -->

# Release notes for Grafana 8.5.0-beta1

### Features and enhancements

- Add config option to enable/disable reporting. (Enterprise)
- **Alerting:** Accurately set value for prom-compatible APIs. [#47216](https://github.com/grafana/grafana/pull/47216), [@gotjosh](https://github.com/gotjosh)
- **Alerting:** Provisioning API - Notification Policies. [#46755](https://github.com/grafana/grafana/pull/46755), [@alexweav](https://github.com/alexweav)
- **Analytics:** Enable grafana and plugin update checks to be operated independently. [#46352](https://github.com/grafana/grafana/pull/46352), [@wbrowne](https://github.com/wbrowne)
- **Azure Monitor:** Add support for multiple template variables in resource picker. [#46215](https://github.com/grafana/grafana/pull/46215), [@sarahzinger](https://github.com/sarahzinger)
- **Caching:** Add separate TTL for resources cache. (Enterprise)
- **Caching:** add support for TLS configuration for Redis Cluster. (Enterprise)
- **NewsPanel:** Remove Use Proxy option and update documentation with recommendations. [#47189](https://github.com/grafana/grafana/pull/47189), [@joshhunt](https://github.com/joshhunt)
- **OAuth:** Sync GitHub OAuth user name to Grafana if it's set. [#45438](https://github.com/grafana/grafana/pull/45438), [@pallxk](https://github.com/pallxk)

### Bug fixes

- **Plugins:** Fix Default Nav URL for dashboard includes. [#47143](https://github.com/grafana/grafana/pull/47143), [@wbrowne](https://github.com/wbrowne)

### Breaking changes

When user is using Github OAuth, GitHub login is showed as both Grafana login and name. Now the GitHub name is showed as Grafana name, and GitHub login is showed as Grafana Login. Issue [#45438](https://github.com/grafana/grafana/issues/45438)

The meaning of the default data source has now changed from being a persisted property in a panel. Before when you selected the default data source for a panel and later changed the default data source to another data source it would change all panels who were configured to use the default data source. From now on the default data source is just the default for new panels and changing the default will not impact any currently saved dashboards. Issue [#45132](https://github.com/grafana/grafana/issues/45132)