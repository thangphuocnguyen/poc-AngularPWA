# POC

## Targets

Bootstrap Simple App in combined with:

* PWA - Progressive Web Application
* Angular (v7+)
* Angular CLI (v7)
* [Angular Material UI](https://material.angular.io/)
* Devices [iOS (Safari) | Android (Chrome) ]

* Amazon Cloudformation
* Amazon S3
* Amazon CloudFront
* AWS Amplify
* AWS Amplify CLI
* Authentication with:
    + Amazon Cognito User Pools
    + Social Federation

* Others *(`not in main focus`)*
    + SCSS
    + Typescript
    + HammerJS for gesture recognition
    + Web application manifest
    + Service worker

## Requirements

* [Node.js 8.11+](https://nodejs.org)
* [AWS Amplify JS 1.x](https://aws-amplify.github.io/media/get_started)
* [AWS Amplify CLI 0.1.x](https://aws-amplify.github.io/media/get_started)
* [Angular 7.x](https://angular.io)
* [Angular CLI 7.x](https://cli.angular.io)
* [Angular Material 7.x](https://material.angular.io)


# AngularPWA

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 8.1.2.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).

# AWS Amplify Development Guidelines

Follow the [Amplify Init Process](https://aws-amplify.github.io/docs/cli-toolchain/quickstart?sdk=js) or follow below steps:

1. Install Amplify CLI as global

    ```$ npm install -g @aws-amplify/cli```

2. Update Amplify Configure (AWS account credentials and IAM user, Project Configure)

    2.1. Re-configure project!

    ```$ amplify configure project```

    2.2. Add hosting for application

    ```$ amplify add hosting```

    > Notice: Since Service workers require a secure origin HTTPs so pls consider to use the option of `PROD (S3 with CloudFront using HTTPS)`

3. Publish Application

    ```$ amplify publish```

> When deploying another version of your application, you need to invalidate the CloudFront cache so that new version can displays right away

```$ amplify publish -c```
