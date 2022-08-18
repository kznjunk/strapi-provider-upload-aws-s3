# strapi-provider-upload-aws-s3

Based on ![https://github.com/strapi/strapi/blob/master/packages/providers/upload-aws-s3/lib/index.js](@strapi/provider-upload-aws-s3)
but with the cdn option:

```js
module.exports = ({ env }) => ({
    upload: {
        config: {
        	...
            provider: 'strapi-provider-upload-aws-s3',
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
