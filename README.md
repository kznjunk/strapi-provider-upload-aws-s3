# strapi-provider-upload-aws-s3

`npm i @kznjunk/strapi-provider-upload-aws-s3 --save`

Based on [@strapi/provider-upload-aws-s3](https://github.com/strapi/strapi/blob/master/packages/providers/upload-aws-s3/lib/index.js)
but with the cdn option:

```js
module.exports = ({ env }) => ({
    upload: {
        config: {
        	...
            provider: '@kznjunk/strapi-provider-upload-aws-s3',
            providerOptions: {
                accessKeyId: env('AWS_ACCESS_KEY_ID'),
                secretAccessKey: env('AWS_ACCESS_SECRET'),
                region: env('AWS_REGION'),
                params: {
                    Bucket: env('AWS_BUCKET'),
                },
                cdn: env('AWS_CDN'),
            },
            ...
        }
    }
})
```
