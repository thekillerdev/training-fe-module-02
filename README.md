# Backbase Training Exercise

## Portal Frontend - Module 2: Widget Extras

In this module, we dive into more advanced widget concepts. We will first look at Camel routes and how they can help us transforming and rendering external content. We will then talk about developing your own ICE templates to render custom content. Finally, we will learn everything about widget chromes and how to develop your own.

### Contents

 - **pf2e1a**: How to consume from a Camel route and g:include the response in a widget ([solution](cxp-fe-training-02/src/main/webapp/static/cxp-fe-training-02/widgets/pf2e1a-feed-reader))
 - **pf2e1b**: How to consume from a Camel route through an ajax call ([solution](cxp-fe-training-02/src/main/webapp/static/cxp-fe-training-02/widgets/pf2e1b-feed-reader))
 - **pf2e2**: How to create ICE templates ([solution](cxp-fe-training-02/src/main/webapp/static/cxp-fe-training-02/widgets/pf2e2-content))
 - **pf2e3**: How to create widget chromes ([solution](cxp-fe-training-02/src/main/webapp/static/cxp-fe-training-02/html/chromes))

### Installation & Configuration

 - Copy and paste the **cxp-fe-training-02** folder in the **statics/bundles** folder of your Launchpad 0.12.x project

 - Add the bundle resource base in **portal/pom.xml**, e.g.:

```xml
<resourceBases>
    <resourceBase>${statics.dir}/bundles/cxp-fe-training-02/src/main/webapp</resourceBase> // add this line
    <resourceBase>${project.basedir}/src/main/webapp</resourceBase>
    <resourceBase>${work.dir}</resourceBase>
</resourceBases>
```

 - Create a folder called **services** at the root of your project, and paste the **feed-service-module** folder in there

 - run `mvn clean install` in the **services/feed-service-module** folder
 - in **portal/pom.xml**, add the following dependency:

```xml
<dependency>
    <groupId>com.backbase.practices</groupId>
    <artifactId>feed-service-module</artifactId>
    <version>1.0-SNAPSHOT</version>
</dependency>
```

Then restart portal.
