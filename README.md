# Script to Allocate Spots Automatically

Developed for KTH Racketklubb.

## Dependency

- Jupyter Notebook

## Feature: Confirmation Emails in Batch

### Configuration

- `client_id`, `client_secret` for authorization
- `email_template`: filename of a basic HTML of the emails for further filling in information of sessions
- `session_time`: time for a specific session
- `session_info`: address info of the venue
- `meeting_place`
- `meeting_time`

### Usage

Given a list of emails of people who got spots for a session, `email_l`, call the function `send_message_receivers`, which will format the email and send confirmation to all receivers.

```
send_message_receivers(
    email_l,
    format_email(
        session_time='Tuesday, 9th of Nov, 22-23h',
        session_info='Tennisstadion (Södra Fiskartorpsvägen 20 114 33 Stockholm).',
        meeting_place='court D14',
        meeting_time='22h'
    )
)
```


## TODO

- Executable version
- More reasonable algorithm to allocate spots

## Reminder

- `client_secret` for sending email will expire in six months.

