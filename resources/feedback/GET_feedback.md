# Feedback Resources
    GET feedback

## Description
Returns a listing of feedbacks in the platform.

## Requires authentication
- Details described [here](/README.md#authentication)

## Parameters
- `page` _(optional)_ - page number for pagination, default 1.
- `per_page` _(optional)_ - items to be returned per page, default 15.

## Example
**Request**

    GET https://api.platform.onesky.io/1/project/:project_id/feedback

**Response**
``` json
{
    "feedbacks": [
        (
            "id":"123",
            "created_at":"2013-03-03T03:03:03+0000".
            "created_at_timestamp":1362301383,
            "url":"http://www.oneskyapp.com",
            "locale":"ja_JP".
            "screenshot_url":"<screen shot url>",
            "submitter_user_type":"employee",
            "submitter_email:"contact@oneskyapp.com",
            "comment":"onesky is good",
            "status":"in-progress",
            "blocks": [
                {"id":"1"},
                {"id":"2"},
            ]
        },
        (
            "id":"456",
            "created_at":"2013-03-04T04:04:04+0000".
            "created_at_timestamp":1365066244,
            "url":"http://www.oneskyapp.com",
            "locale":"zh_CN".
            "screenshot_url":"<screen shot url>",
            "submitter_user_type":"proofreader",
            "submitter_email:"contact@oneskyapp.com",
            "comment":"I love onesky",
            "status":"finished",
            "blocks": [
                {"id":"7"},
                {"id":"8"},
                {"id":"9"}
            ]
        }
    ]
}
```