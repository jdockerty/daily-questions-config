# Daily Questions Confg

This is repository hosts the configuration files for the [daily-questions](https://github.com/jdockerty/daily-questions) application.

The main usage of this repository is for the Kubernetes manifest, contained within the `kubernetes` directory; this defines a `CronJob` object for which the application runs. The configuration is stored within an encrypted `SealedSecret` object, the public certificate of the Bitnami Sealed Secrets controller was retrieved using `kubeseal --fetch-cert > cert.pem`, this is the public key, and used locally to encrypt the raw configuration for the application.