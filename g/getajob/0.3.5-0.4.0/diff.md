# Comparing `tmp/getajob-0.3.5.tar.gz` & `tmp/getajob-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "getajob-0.3.5.tar", max compression
+gzip compressed data, was "getajob-0.4.0.tar", max compression
```

## Comparing `getajob-0.3.5.tar` & `getajob-0.4.0.tar`

### file list

```diff
@@ -1,130 +1,145 @@
--rw-r--r--   0        0        0    11357 2023-07-20 00:49:20.063478 getajob-0.3.5/LICENSE
--rw-r--r--   0        0        0       69 2023-07-20 00:49:20.063478 getajob-0.3.5/README.md
--rw-r--r--   0        0        0       22 2023-07-20 00:49:20.063478 getajob-0.3.5/getajob/__init__.py
--rw-r--r--   0        0        0     2372 2023-07-20 00:49:20.063478 getajob-0.3.5/getajob/abstractions/models.py
--rw-r--r--   0        0        0    14436 2023-07-20 00:49:20.063478 getajob-0.3.5/getajob/abstractions/repository.py
--rw-r--r--   0        0        0      385 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/abstractions/vendor_client_factory.py
--rw-r--r--   0        0        0     1740 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/config/settings.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/__init__.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/admin/__init__.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/admin/search/__init__.py
--rw-r--r--   0        0        0      141 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/admin/search/models.py
--rw-r--r--   0        0        0      406 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/admin/search/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/admin/users/__init__.py
--rw-r--r--   0        0        0      620 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/admin/users/models.py
--rw-r--r--   0        0        0      684 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/admin/users/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/applications/__init__.py
--rw-r--r--   0        0        0      188 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/applications/enumerations.py
--rw-r--r--   0        0        0      726 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/applications/models.py
--rw-r--r--   0        0        0     3187 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/applications/repository.py
--rw-r--r--   0        0        0     2176 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/applications/unit_of_work.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/__init__.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/details/__init__.py
--rw-r--r--   0        0        0      425 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/details/models.py
--rw-r--r--   0        0        0      686 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/details/repository.py
--rw-r--r--   0        0        0     1870 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/enumerations.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/invitations/__init__.py
--rw-r--r--   0        0        0      145 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/invitations/models.py
--rw-r--r--   0        0        0      653 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/invitations/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/jobs/__init__.py
--rw-r--r--   0        0        0     3110 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/jobs/models.py
--rw-r--r--   0        0        0     1219 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/jobs/repository.py
--rw-r--r--   0        0        0      533 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/jobs/unit_of_work.py
--rw-r--r--   0        0        0      102 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/models.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/recruiters/__init__.py
--rw-r--r--   0        0        0      117 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/recruiters/models.py
--rw-r--r--   0        0        0      581 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/recruiters/repository.py
--rw-r--r--   0        0        0      813 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/companies/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/scheduled_events/__init__.py
--rw-r--r--   0        0        0      210 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/scheduled_events/enumerations.py
--rw-r--r--   0        0        0      995 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/scheduled_events/models.py
--rw-r--r--   0        0        0     1659 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/scheduled_events/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/static/__init__.py
--rw-r--r--   0        0        0     1327 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/static/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/contact_info/__init__.py
--rw-r--r--   0        0        0      417 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/contact_info/models.py
--rw-r--r--   0        0        0      718 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/contact_info/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/cover_letters/__init__.py
--rw-r--r--   0        0        0      277 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/cover_letters/models.py
--rw-r--r--   0        0        0      691 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/cover_letters/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/demographics/__init__.py
--rw-r--r--   0        0        0      916 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/demographics/models.py
--rw-r--r--   0        0        0      682 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/demographics/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/enumerations.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/job_preferences/__init__.py
--rw-r--r--   0        0        0     1653 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/job_preferences/models.py
--rw-r--r--   0        0        0      712 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/job_preferences/repository.py
--rw-r--r--   0        0        0       89 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/models.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/qualifications/__init__.py
--rw-r--r--   0        0        0     2592 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/qualifications/models.py
--rw-r--r--   0        0        0      681 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/qualifications/repository.py
--rw-r--r--   0        0        0      632 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/resumes/__init__.py
--rw-r--r--   0        0        0      196 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/resumes/models.py
--rw-r--r--   0        0        0      637 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/resumes/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/sessions/__init__.py
--rw-r--r--   0        0        0      376 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/contexts/users/sessions/models.py
--rw-r--r--   0        0        0     2463 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/exceptions.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/static/__init__.py
--rw-r--r--   0        0        0      362 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/static/enumerations.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/test_support/__init__.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/test_support/fixtures/__init__.py
--rw-r--r--   0        0        0     1975 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/test_support/fixtures/application.py
--rw-r--r--   0        0        0     1005 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/test_support/fixtures/company.py
--rw-r--r--   0        0        0      360 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/test_support/fixtures/job.py
--rw-r--r--   0        0        0      557 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/test_support/fixtures/recruiter.py
--rw-r--r--   0        0        0      623 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/test_support/fixtures/recruiter_invitation.py
--rw-r--r--   0        0        0     1684 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/test_support/fixtures/scheduled_events.py
--rw-r--r--   0        0        0     2398 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/test_support/fixtures/users.py
--rw-r--r--   0        0        0      375 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/utils.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/__init__.py
--rw-r--r--   0        0        0      165 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/aiocron.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/algolia/__init__.py
--rw-r--r--   0        0        0      468 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/algolia/client_factory.py
--rw-r--r--   0        0        0      835 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/algolia/mock.py
--rw-r--r--   0        0        0      702 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/algolia/models.py
--rw-r--r--   0        0        0     1189 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/algolia/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/__init__.py
--rw-r--r--   0        0        0     2139 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/client.py
--rw-r--r--   0        0        0      340 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/client_factory.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/companies/__init__.py
--rw-r--r--   0        0        0      894 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/companies/models.py
--rw-r--r--   0        0        0     1972 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/companies/repository.py
--rw-r--r--   0        0        0     2553 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/mock.py
--rw-r--r--   0        0        0      413 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/models.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/recruiter_invitation/__init__.py
--rw-r--r--   0        0        0      747 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/recruiter_invitation/models.py
--rw-r--r--   0        0        0     2040 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/recruiter_invitation/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/recruiters/__init__.py
--rw-r--r--   0        0        0     1588 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/recruiters/models.py
--rw-r--r--   0        0        0     2391 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/recruiters/repository.py
--rw-r--r--   0        0        0     2318 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/users/__init__.py
--rw-r--r--   0        0        0     1320 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/users/models.py
--rw-r--r--   0        0        0     1963 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/clerk/users/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/firestore/__init__.py
--rw-r--r--   0        0        0      582 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/firestore/client_factory.py
--rw-r--r--   0        0        0     1102 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/firestore/helpers.py
--rw-r--r--   0        0        0      507 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/firestore/mock.py
--rw-r--r--   0        0        0     1975 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/firestore/models.py
--rw-r--r--   0        0        0     9100 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/firestore/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/kafka/__init__.py
--rw-r--r--   0        0        0      725 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/kafka/authentication.py
--rw-r--r--   0        0        0     1369 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/kafka/client_factory.py
--rw-r--r--   0        0        0      320 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/kafka/exceptions.py
--rw-r--r--   0        0        0      617 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/kafka/mock.py
--rw-r--r--   0        0        0     1480 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/kafka/models.py
--rw-r--r--   0        0        0     1517 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/kafka/repository.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/openai/__init__.py
--rw-r--r--   0        0        0      443 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/openai/client_factory.py
--rw-r--r--   0        0        0      690 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/openai/mock.py
--rw-r--r--   0        0        0      985 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/openai/repository.py
--rw-r--r--   0        0        0      590 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/openai/settings.py
--rw-r--r--   0        0        0        0 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/sendgrid/__init__.py
--rw-r--r--   0        0        0      420 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/sendgrid/client_factory.py
--rw-r--r--   0        0        0      227 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/sendgrid/mock.py
--rw-r--r--   0        0        0      678 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/sendgrid/repository.py
--rw-r--r--   0        0        0       45 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/sendgrid/templates/example.html
--rw-r--r--   0        0        0      251 2023-07-20 00:49:20.067478 getajob-0.3.5/getajob/vendor/sentry.py
--rw-r--r--   0        0        0     1769 2023-07-20 00:49:20.071478 getajob-0.3.5/pyproject.toml
--rw-r--r--   0        0        0     2854 1970-01-01 00:00:00.000000 getajob-0.3.5/PKG-INFO
+-rw-r--r--   0        0        0    11357 2023-07-23 19:54:05.337152 getajob-0.4.0/LICENSE
+-rw-r--r--   0        0        0       69 2023-07-23 19:54:05.337152 getajob-0.4.0/README.md
+-rw-r--r--   0        0        0       22 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/__init__.py
+-rw-r--r--   0        0        0     2653 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/abstractions/models.py
+-rw-r--r--   0        0        0    14701 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/abstractions/repository.py
+-rw-r--r--   0        0        0      385 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/abstractions/vendor_client_factory.py
+-rw-r--r--   0        0        0     1993 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/config/settings.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/admin/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/admin/search/__init__.py
+-rw-r--r--   0        0        0      141 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/admin/search/models.py
+-rw-r--r--   0        0        0      451 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/admin/search/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/admin/users/__init__.py
+-rw-r--r--   0        0        0      620 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/admin/users/models.py
+-rw-r--r--   0        0        0      803 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/admin/users/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/applications/__init__.py
+-rw-r--r--   0        0        0      188 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/applications/enumerations.py
+-rw-r--r--   0        0        0      726 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/applications/models.py
+-rw-r--r--   0        0        0     3429 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/applications/repository.py
+-rw-r--r--   0        0        0     2176 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/applications/unit_of_work.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/chat/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/chat/message/__init__.py
+-rw-r--r--   0        0        0      616 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/chat/message/models.py
+-rw-r--r--   0        0        0      848 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/chat/message/repository.py
+-rw-r--r--   0        0        0      272 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/chat/models.py
+-rw-r--r--   0        0        0     1372 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/chat/repository.py
+-rw-r--r--   0        0        0     1650 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/chat/unit_of_work.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/audit/__init__.py
+-rw-r--r--   0        0        0      482 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/audit/models.py
+-rw-r--r--   0        0        0     1060 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/audit/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/details/__init__.py
+-rw-r--r--   0        0        0      425 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/details/models.py
+-rw-r--r--   0        0        0      805 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/details/repository.py
+-rw-r--r--   0        0        0     1870 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/enumerations.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/invitations/__init__.py
+-rw-r--r--   0        0        0      145 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/invitations/models.py
+-rw-r--r--   0        0        0      742 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/invitations/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/jobs/__init__.py
+-rw-r--r--   0        0        0     3153 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/jobs/models.py
+-rw-r--r--   0        0        0     1357 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/jobs/repository.py
+-rw-r--r--   0        0        0      533 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/jobs/unit_of_work.py
+-rw-r--r--   0        0        0      102 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/models.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/recruiters/__init__.py
+-rw-r--r--   0        0        0      117 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/recruiters/models.py
+-rw-r--r--   0        0        0      700 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/recruiters/repository.py
+-rw-r--r--   0        0        0      864 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/companies/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/scheduled_events/__init__.py
+-rw-r--r--   0        0        0      210 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/scheduled_events/enumerations.py
+-rw-r--r--   0        0        0      995 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/scheduled_events/models.py
+-rw-r--r--   0        0        0     1821 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/scheduled_events/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/static/__init__.py
+-rw-r--r--   0        0        0     1327 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/static/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/contact_info/__init__.py
+-rw-r--r--   0        0        0      417 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/contact_info/models.py
+-rw-r--r--   0        0        0      807 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/contact_info/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/cover_letters/__init__.py
+-rw-r--r--   0        0        0      277 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/cover_letters/models.py
+-rw-r--r--   0        0        0      870 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/cover_letters/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/demographics/__init__.py
+-rw-r--r--   0        0        0      916 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/demographics/models.py
+-rw-r--r--   0        0        0      861 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/demographics/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/enumerations.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/job_preferences/__init__.py
+-rw-r--r--   0        0        0     1653 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/job_preferences/models.py
+-rw-r--r--   0        0        0      801 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/job_preferences/repository.py
+-rw-r--r--   0        0        0       89 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/models.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/qualifications/__init__.py
+-rw-r--r--   0        0        0     2592 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/qualifications/models.py
+-rw-r--r--   0        0        0      860 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/qualifications/repository.py
+-rw-r--r--   0        0        0      937 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/resumes/__init__.py
+-rw-r--r--   0        0        0      196 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/resumes/models.py
+-rw-r--r--   0        0        0      816 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/resumes/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/sessions/__init__.py
+-rw-r--r--   0        0        0      481 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/contexts/users/sessions/models.py
+-rw-r--r--   0        0        0     2607 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/exceptions.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/static/__init__.py
+-rw-r--r--   0        0        0      362 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/static/enumerations.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/test_support/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/test_support/fixtures/__init__.py
+-rw-r--r--   0        0        0     2116 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/test_support/fixtures/application.py
+-rw-r--r--   0        0        0     1684 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/test_support/fixtures/chat.py
+-rw-r--r--   0        0        0     1027 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/test_support/fixtures/company.py
+-rw-r--r--   0        0        0      382 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/test_support/fixtures/job.py
+-rw-r--r--   0        0        0     1843 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/test_support/fixtures/recruiter.py
+-rw-r--r--   0        0        0      645 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/test_support/fixtures/recruiter_invitation.py
+-rw-r--r--   0        0        0     1706 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/test_support/fixtures/scheduled_events.py
+-rw-r--r--   0        0        0     2442 2023-07-23 19:54:05.337152 getajob-0.4.0/getajob/test_support/fixtures/users.py
+-rw-r--r--   0        0        0      594 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/utils.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/__init__.py
+-rw-r--r--   0        0        0      165 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/aiocron.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/algolia/__init__.py
+-rw-r--r--   0        0        0      468 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/algolia/client_factory.py
+-rw-r--r--   0        0        0     1258 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/algolia/mock.py
+-rw-r--r--   0        0        0      702 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/algolia/models.py
+-rw-r--r--   0        0        0     1545 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/algolia/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/__init__.py
+-rw-r--r--   0        0        0     2139 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/client.py
+-rw-r--r--   0        0        0      340 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/client_factory.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/companies/__init__.py
+-rw-r--r--   0        0        0      894 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/companies/models.py
+-rw-r--r--   0        0        0     2110 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/companies/repository.py
+-rw-r--r--   0        0        0     2553 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/mock.py
+-rw-r--r--   0        0        0      413 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/models.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/recruiter_invitation/__init__.py
+-rw-r--r--   0        0        0      747 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/recruiter_invitation/models.py
+-rw-r--r--   0        0        0     2043 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/recruiter_invitation/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/recruiters/__init__.py
+-rw-r--r--   0        0        0     1588 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/recruiters/models.py
+-rw-r--r--   0        0        0     2371 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/recruiters/repository.py
+-rw-r--r--   0        0        0     2318 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/users/__init__.py
+-rw-r--r--   0        0        0     1320 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/users/models.py
+-rw-r--r--   0        0        0     2101 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/clerk/users/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/firestore/__init__.py
+-rw-r--r--   0        0        0      582 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/firestore/client_factory.py
+-rw-r--r--   0        0        0     1102 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/firestore/helpers.py
+-rw-r--r--   0        0        0      507 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/firestore/mock.py
+-rw-r--r--   0        0        0     1975 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/firestore/models.py
+-rw-r--r--   0        0        0     9100 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/firestore/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/kafka/__init__.py
+-rw-r--r--   0        0        0      725 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/kafka/authentication.py
+-rw-r--r--   0        0        0     1369 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/kafka/client_factory.py
+-rw-r--r--   0        0        0      320 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/kafka/exceptions.py
+-rw-r--r--   0        0        0      664 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/kafka/mock.py
+-rw-r--r--   0        0        0     1843 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/kafka/models.py
+-rw-r--r--   0        0        0     1517 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/kafka/repository.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/mailgun/__init__.py
+-rw-r--r--   0        0        0      989 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/mailgun/client_factory.py
+-rw-r--r--   0        0        0      282 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/mailgun/mock.py
+-rw-r--r--   0        0        0     1233 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/mailgun/repository.py
+-rw-r--r--   0        0        0      104 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/mailgun/templates/chat_message.html
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/openai/__init__.py
+-rw-r--r--   0        0        0      443 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/openai/client_factory.py
+-rw-r--r--   0        0        0      690 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/openai/mock.py
+-rw-r--r--   0        0        0      985 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/openai/repository.py
+-rw-r--r--   0        0        0      590 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/openai/settings.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/redis/__init__.py
+-rw-r--r--   0        0        0      502 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/redis/client_factory.py
+-rw-r--r--   0        0        0      343 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/redis/mock.py
+-rw-r--r--   0        0        0     2129 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/redis/repository.py
+-rw-r--r--   0        0        0      251 2023-07-23 19:54:05.341152 getajob-0.4.0/getajob/vendor/sentry.py
+-rw-r--r--   0        0        0     1786 2023-07-23 19:54:05.341152 getajob-0.4.0/pyproject.toml
+-rw-r--r--   0        0        0     2892 1970-01-01 00:00:00.000000 getajob-0.4.0/PKG-INFO
```

### Comparing `getajob-0.3.5/LICENSE` & `getajob-0.4.0/LICENSE`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/abstractions/models.py` & `getajob-0.4.0/getajob/abstractions/models.py`

 * *Files 6% similar despite different names*

```diff
@@ -47,20 +47,24 @@
     update: bool = True
     delete: bool = True
 
 
 class Entity(str, Enum):
     USERS = "users"  # Comes from clerk
     USER_DETAILS = "user_details"  # What we add to user data
+    USER_MEMBERSHIPS = "user_memberships"
+    CHAT = "chat"
+    CHAT_MESSAGES = "chat_messages"
     ADMIN_USERS = "admin_users"
     SKILLS = "skills"
     COVER_LETTERS = "cover_letters"
     RESUMES = "resumes"
     COMPANIES = "companies"  # Comes from clerk
     COMPANY_DETAILS = "company_details"  # What we add to company data
+    COMPANY_AUDITS = "company_audits"
     RECRUITERS = "recruiters"  # Comes from clerk
     RECRUITER_INVITATIONS = "recruiter_invitations"  # Comes from clerk
     RECRUITER_DETAILS = "recruiter_details"  # What we add to recruiter data
     JOBS = "jobs"
     APPLICATIONS = "applications"
     USER_NOTIFICATIONS = "user_notifications"
     SCHEDULED_EVENTS = "scheduled_events"
@@ -81,12 +85,21 @@
     country: str
     lat: float
     lon: float
 
 
 @dataclass
 class RepositoryDependencies:
+    user_id: str
     db: FirestoreDB
     collection_name: str
     entity_models: EntityModels
     kafka: t.Optional[KafkaProducerRepository] = None
     kafka_event_config: t.Optional[KafkaEventConfig] = None
+
+
+@dataclass
+class UserAndDatabaseConnection:
+    """Created during a request"""
+
+    initiating_user_id: str
+    db: FirestoreDB
```

### Comparing `getajob-0.3.5/getajob/abstractions/repository.py` & `getajob-0.4.0/getajob/abstractions/repository.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import typing as t
 from datetime import datetime
 from functools import wraps
-
 from pydantic import BaseModel
 
+from getajob.abstractions.models import BaseDataModel
 from getajob.utils import generate_random_short_code
 from getajob.exceptions import (
     KafkaEventTopicNotProvidedError,
     EntityNotFound,
     MissingParentKeyError,
 )
 from getajob.vendor.firestore.models import (
@@ -32,20 +32,20 @@
     BaseDataModel,
     RepositoryDependencies,
 )
 
 
 def format_to_schema(
     document: FirestoreDocument, entity_model: t.Type[BaseModel]
-) -> BaseModel:
+) -> BaseDataModel:
     id_included_dict = {
         "id": document.id,
         **document.data,
     }
-    return entity_model(**id_included_dict)
+    return t.cast(BaseDataModel, entity_model(**id_included_dict))
 
 
 def format_paginated_response(
     res: FirestorePaginatedResponse, entity_model: t.Optional[t.Type[BaseModel]] = None
 ):
     if entity_model is None:
         data = [
@@ -142,68 +142,73 @@
     ):
         self.db = dependencies.db
         self.collection_name = dependencies.collection_name
         self.entity_models = dependencies.entity_models
         self.kafka = dependencies.kafka
         self.kafka_event_config = dependencies.kafka_event_config
         self.required_parent_keys = required_parent_keys
+        self.requesting_user_id = dependencies.user_id
 
         # If kafka client given but with no configuration, complain about it
         if self.kafka and not self.kafka_event_config:
             raise KafkaEventTopicNotProvidedError()
 
     def _produce_repository_kafka_event(
-        self, event_type: KafkaEventType, object_id: str, data: dict | None = None
+        self,
+        event_type: KafkaEventType,
+        object_id: str,
+        data: dict | None = None,
     ):
         if (
             not self.kafka
             or not self.kafka_event_config
             or not self.kafka_event_config.dict()[event_type]
         ):
             return
         self.kafka.publish(
             topic=self.kafka_event_config.topic,
             message=BaseKafkaMessage(
                 message_type=f"{event_type.value}_{self.collection_name}",
+                requesting_user_id=self.requesting_user_id,
                 object_id=object_id,
                 data=data if data else None,
             ),
         )
 
     @ensure_parent_keys
     def get(
         self,
         doc_id: str,
         parent_collections: dict = {},
         internal_get_request: bool = False,
-    ) -> BaseModel:
+    ) -> BaseDataModel:
         res = self.db.get(parent_collections, self.collection_name, doc_id)
         if not internal_get_request:
             self._produce_repository_kafka_event(KafkaEventType.get, doc_id)
         return format_to_schema(res, self.entity_models.entity)
 
     @ensure_parent_keys
     def get_with_filters(
         self,
         doc_id: str,
         filters: t.List[FirestoreFilters],
         parent_collections: dict = {},
-    ) -> BaseModel:
+    ) -> BaseDataModel:
         res = self.db.get_with_filters(
             parent_collections, self.collection_name, doc_id, filters
         )
         return format_to_schema(res, self.entity_models.entity)
 
     @ensure_parent_keys
     def create(
         self,
         data: BaseModel,
         parent_collections: dict = {},
         provided_id: t.Optional[str] = None,
-    ) -> BaseModel:
+    ) -> BaseDataModel:
         data_dict = data.dict()
         data_dict.update(
             {
                 "created": datetime.now(),
                 "updated": datetime.now(),
             }
         )
@@ -219,15 +224,15 @@
 
     @ensure_parent_keys
     def update(
         self,
         doc_id: str,
         data: BaseModel,
         parent_collections: dict = {},
-    ) -> BaseModel:
+    ) -> BaseDataModel:
         original_item = self.get(doc_id, parent_collections, True).dict()
         for key, val in data.dict().items():
             if val is not None:
                 original_item[key] = val
         original_item["updated"] = datetime.now()
         res = self.db.update(
             parent_collections, self.collection_name, doc_id, original_item
@@ -241,25 +246,27 @@
     def delete(
         self,
         doc_id: str,
         parent_collections: dict = {},
     ) -> bool:
         deleted_object = self.get(doc_id, parent_collections, True)
         self._produce_repository_kafka_event(
-            KafkaEventType.delete, doc_id, deleted_object.dict()
+            KafkaEventType.delete,
+            doc_id,
+            deleted_object.dict(),
         )
         return self.db.delete(parent_collections, self.collection_name, doc_id)
 
     @ensure_parent_keys
     def get_one_by_attribute(
         self,
         attribute: str,
         value: t.Any,
         parent_collections: dict = {},
-    ) -> t.Union[BaseModel, None]:
+    ) -> t.Union[BaseDataModel, None]:
         res = self.db.get_one_by_attribute(
             parent_collections, self.collection_name, attribute, value
         )
         return format_to_schema(res, self.entity_models.entity)
 
     @ensure_parent_keys
     def query(
```

### Comparing `getajob-0.3.5/getajob/config/settings.py` & `getajob-0.4.0/getajob/config/settings.py`

 * *Files 9% similar despite different names*

```diff
@@ -36,20 +36,26 @@
 
     # Kafka config
     KAFKA_BOOTSTRAP_SERVER: str = os.getenv("KAFKA_BOOTSTRAP_SERVER", "")
     KAFKA_USERNAME: str = os.getenv("KAFKA_USERNAME", "")
     KAFKA_PASSWORD: str = os.getenv("KAFKA_PASSWORD", "")
     KAFKA_JWT_SECRET: str = os.getenv("KAFKA_JWT_SECRET", "")
 
-    # Sendgrid config
-    SENDGRID_API_KEY: str = os.getenv("SENDGRID_API_KEY", "")
-    SENDGRID_FROM_EMAIL: str = os.getenv("SENDGRID_FROM_EMAIL", "")
+    # Mailgun config
+    MAILGUN_API_KEY: str = os.getenv("MAILGUN_API_KEY", "")
+    MAILGUN_BASE_API_URL: str = os.getenv("MAILGUN_BASE_API_URL", "")
+    MAILGUN_FROM_EMAIL: str = os.getenv("MAILGUN_FROM_EMAIL", "")
 
     # Sentry config
     SENTRY_DSN: str = os.getenv("SENTRY_DSN", "")
     SENTRY_TRACES_RATE: float = 1.0
 
+    # Redis config
+    REDIS_HOST: str = os.getenv("REDIS_HOST", "")
+    REDIS_PORT: int = int(os.getenv("REDIS_PORT", "39004"))
+    REDIS_PASSWORD: str = os.getenv("REDIS_PASSWORD", "")
+
     class Config:
         env_file = ".env"
 
 
 SETTINGS = AppSettings()  # type: ignore
```

### Comparing `getajob-0.3.5/getajob/contexts/admin/users/models.py` & `getajob-0.4.0/getajob/contexts/admin/users/models.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/contexts/applications/models.py` & `getajob-0.4.0/getajob/contexts/applications/models.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/contexts/applications/repository.py` & `getajob-0.4.0/getajob/contexts/applications/repository.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,46 +1,54 @@
 import typing as t
 
 from getajob.abstractions.models import Entity
 from getajob.abstractions.repository import ParentRepository, RepositoryDependencies
 from getajob.vendor.firestore.models import FirestoreFilters
-from getajob.vendor.firestore.repository import FirestoreDB
+from getajob.abstractions.models import UserAndDatabaseConnection
 from getajob.vendor.kafka.repository import KafkaProducerRepository
 from getajob.vendor.kafka.models import KafkaEventConfig, KafkaTopic
 from getajob.contexts.users.resumes.repository import ResumeRepository
 from getajob.contexts.companies.jobs.repository import JobsRepository
 
 from .models import entity_models, UserCreatedApplication
 from .unit_of_work import ApplicationsUnitOfWork
 
 
 class ApplicationRepository(ParentRepository):
     def __init__(
-        self, db: FirestoreDB, kafka: t.Optional[KafkaProducerRepository] = None
+        self,
+        request_scope: UserAndDatabaseConnection,
+        kafka: t.Optional[KafkaProducerRepository] = None,
     ):
+        self.request_scope = request_scope
         kafka_event_config = KafkaEventConfig(
             topic=KafkaTopic.applications,
             create=True,
             update=True,
             delete=True,
             get=True,
         )
         super().__init__(
             RepositoryDependencies(
-                db, Entity.APPLICATIONS.value, entity_models, kafka, kafka_event_config
+                request_scope.initiating_user_id,
+                request_scope.db,
+                Entity.APPLICATIONS.value,
+                entity_models,
+                kafka,
+                kafka_event_config,
             ),
         )
 
     def user_creates_application(
         self, user_id: str, application: UserCreatedApplication
     ):
         return ApplicationsUnitOfWork(self).user_creates_application(
             user_id=user_id,
-            resume_repo=ResumeRepository(self.db),
-            job_repo=JobsRepository(self.db),
+            resume_repo=ResumeRepository(self.request_scope),
+            job_repo=JobsRepository(self.request_scope),
             create_application=application,
         )
 
     def get_applications_by_company(self, company_id: str):
         return super().query(
             filters=[
                 FirestoreFilters(field="company_id", operator="==", value=company_id),
```

### Comparing `getajob-0.3.5/getajob/contexts/applications/unit_of_work.py` & `getajob-0.4.0/getajob/contexts/applications/unit_of_work.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/contexts/companies/enumerations.py` & `getajob-0.4.0/getajob/contexts/companies/enumerations.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/contexts/companies/invitations/repository.py` & `getajob-0.4.0/getajob/contexts/companies/invitations/repository.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,20 +1,22 @@
-from getajob.vendor.firestore.repository import FirestoreDB
 from getajob.abstractions.repository import (
     MultipleChildrenRepository,
     RepositoryDependencies,
 )
-from getajob.abstractions.models import Entity, EntityModels
+from getajob.abstractions.models import Entity, EntityModels, UserAndDatabaseConnection
 
 from .models import RecruiterInvitation
 
 entity_models = EntityModels(entity=RecruiterInvitation)
 
 
 class RecruiterInvitationsRepository(MultipleChildrenRepository):
-    def __init__(self, db: FirestoreDB):
+    def __init__(self, request_scope: UserAndDatabaseConnection):
         super().__init__(
             RepositoryDependencies(
-                db, Entity.RECRUITER_INVITATIONS.value, entity_models
+                request_scope.initiating_user_id,
+                request_scope.db,
+                Entity.RECRUITER_INVITATIONS.value,
+                entity_models,
             ),
             required_parent_keys=[Entity.COMPANIES.value],
         )
```

### Comparing `getajob-0.3.5/getajob/contexts/companies/jobs/models.py` & `getajob-0.4.0/getajob/contexts/companies/jobs/models.py`

 * *Files 2% similar despite different names*

```diff
@@ -106,7 +106,11 @@
 class InternalUpdateJob(UpdateJob):
     position_filled: t.Optional[bool] = None
     view_count: t.Optional[int] = None
 
 
 class Job(CreateJob, BaseDataModel):
     position_filled: bool = False
+
+
+class KafkaJob(Job):
+    company_id: str
```

### Comparing `getajob-0.3.5/getajob/contexts/companies/jobs/repository.py` & `getajob-0.4.0/getajob/contexts/companies/jobs/repository.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,33 +1,39 @@
 import typing as t
-from getajob.vendor.firestore.repository import FirestoreDB
 from getajob.vendor.kafka.repository import KafkaProducerRepository
 from getajob.vendor.kafka.models import KafkaEventConfig, KafkaTopic
 from getajob.abstractions.repository import (
     MultipleChildrenRepository,
     RepositoryDependencies,
 )
-from getajob.abstractions.models import Entity, EntityModels
+from getajob.abstractions.models import Entity, EntityModels, UserAndDatabaseConnection
 
 from .models import CreateJob, UpdateJob, Job, UserCreateJob
 from .unit_of_work import JobsUnitOfWork
 
 
 entity_models = EntityModels(entity=Job, create=CreateJob, update=UpdateJob)
 
 
 class JobsRepository(MultipleChildrenRepository):
     def __init__(
-        self, db: FirestoreDB, kafka: t.Optional[KafkaProducerRepository] = None
+        self,
+        request_scope: UserAndDatabaseConnection,
+        kafka: t.Optional[KafkaProducerRepository] = None,
     ):
         kafka_event_config = KafkaEventConfig(
             topic=KafkaTopic.jobs, create=True, update=True, delete=True, get=True
         )
         super().__init__(
             RepositoryDependencies(
-                db, Entity.JOBS.value, entity_models, kafka, kafka_event_config
+                request_scope.initiating_user_id,
+                request_scope.db,
+                Entity.JOBS.value,
+                entity_models,
+                kafka,
+                kafka_event_config,
             ),
             required_parent_keys=[Entity.COMPANIES.value],
         )
 
     def create_job(self, company_id: str, job: UserCreateJob):
         return JobsUnitOfWork(self).create_job(company_id, job)
```

### Comparing `getajob-0.3.5/getajob/contexts/companies/jobs/unit_of_work.py` & `getajob-0.4.0/getajob/contexts/companies/jobs/unit_of_work.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/contexts/companies/recruiters/repository.py` & `getajob-0.4.0/getajob/contexts/companies/recruiters/repository.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,18 +1,22 @@
-from getajob.vendor.firestore.repository import FirestoreDB
 from getajob.abstractions.repository import (
     MultipleChildrenRepository,
     RepositoryDependencies,
 )
-from getajob.abstractions.models import Entity, EntityModels
+from getajob.abstractions.models import Entity, EntityModels, UserAndDatabaseConnection
 
 from .models import Recruiter
 
 entity_models = EntityModels(entity=Recruiter)
 
 
 class RecruiterRepository(MultipleChildrenRepository):
-    def __init__(self, db: FirestoreDB):
+    def __init__(self, request_scope: UserAndDatabaseConnection):
         super().__init__(
-            RepositoryDependencies(db, Entity.RECRUITERS.value, entity_models),
+            RepositoryDependencies(
+                request_scope.initiating_user_id,
+                request_scope.db,
+                Entity.RECRUITERS.value,
+                entity_models,
+            ),
             required_parent_keys=[Entity.COMPANIES.value],
         )
```

### Comparing `getajob-0.3.5/getajob/contexts/companies/repository.py` & `getajob-0.4.0/getajob/contexts/companies/repository.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 from getajob.vendor.firestore.models import FirestoreFilters
-from getajob.vendor.firestore.repository import FirestoreDB
 from getajob.abstractions.repository import ParentRepository, RepositoryDependencies
-from getajob.abstractions.models import Entity, EntityModels
+from getajob.abstractions.models import Entity, EntityModels, UserAndDatabaseConnection
 
 from .models import Company
 
 entity_models = EntityModels(entity=Company)
 
 
 class CompanyRepository(ParentRepository):
-    def __init__(self, db: FirestoreDB):
+    def __init__(self, request_scope: UserAndDatabaseConnection):
         super().__init__(
-            RepositoryDependencies(db, Entity.COMPANIES.value, entity_models)
+            RepositoryDependencies(
+                request_scope.initiating_user_id,
+                request_scope.db,
+                Entity.COMPANIES.value,
+                entity_models,
+            )
         )
 
     def get_companies_by_company_id_list(self, company_id_list: list[str]):
         return self.query(
-            filters=[
-                FirestoreFilters(
-                    field="id", operator="in", value=company_id_list
-                )
-            ]
+            filters=[FirestoreFilters(field="id", operator="in", value=company_id_list)]
         )
```

### Comparing `getajob-0.3.5/getajob/contexts/scheduled_events/models.py` & `getajob-0.4.0/getajob/contexts/scheduled_events/models.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/contexts/scheduled_events/repository.py` & `getajob-0.4.0/getajob/contexts/scheduled_events/repository.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,15 +1,14 @@
 from datetime import datetime
 from getajob.vendor.firestore.repository import (
-    FirestoreDB,
     FirestoreFilters,
     FirestorePagination,
 )
 from getajob.abstractions.repository import ParentRepository, RepositoryDependencies
-from getajob.abstractions.models import EntityModels, Entity
+from getajob.abstractions.models import EntityModels, Entity, UserAndDatabaseConnection
 
 from .models import (
     CreateScheduledEvent,
     UpdateScheduledEvent,
     ScheduledEvent,
 )
 
@@ -17,17 +16,22 @@
     entity=ScheduledEvent,
     create=CreateScheduledEvent,
     update=UpdateScheduledEvent,
 )
 
 
 class ScheduledEventsRepository(ParentRepository):
-    def __init__(self, db: FirestoreDB):
+    def __init__(self, request_scope: UserAndDatabaseConnection):
         super().__init__(
-            RepositoryDependencies(db, Entity.SCHEDULED_EVENTS.value, entity_models)
+            RepositoryDependencies(
+                request_scope.initiating_user_id,
+                request_scope.db,
+                Entity.SCHEDULED_EVENTS.value,
+                entity_models,
+            )
         )
 
     def create_scheduled_event(self, data: CreateScheduledEvent):
         data.next_run_time = data.calculate_next_invocation()
         return super().create(data)
 
     def get_current_scheduled_events(self, page: dict | None = None):
```

### Comparing `getajob-0.3.5/getajob/contexts/static/repository.py` & `getajob-0.4.0/getajob/contexts/static/repository.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/contexts/users/contact_info/repository.py` & `getajob-0.4.0/getajob/contexts/users/cover_letters/repository.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,27 +1,27 @@
 from getajob.vendor.firestore.repository import FirestoreDB
 from getajob.abstractions.repository import (
-    SingleChildRepository,
+    MultipleChildrenRepository,
     RepositoryDependencies,
 )
-from getajob.abstractions.models import Entity, EntityModels
-
-from .models import (
-    UserContactInformation,
-    ContactInformation,
-)
+from getajob.abstractions.models import Entity, EntityModels, UserAndDatabaseConnection
 
+from .models import CoverLetter, CreateCoverLetter, UpdateCoverLetter
 
 entity_models = EntityModels(
-    entity=UserContactInformation,
-    create=ContactInformation,
+    entity=CoverLetter,
+    create=CreateCoverLetter,
+    update=UpdateCoverLetter,
 )
 
 
-class ContactInformationRepository(SingleChildRepository):
-    def __init__(self, db: FirestoreDB):
+class CoverLetterRepository(MultipleChildrenRepository):
+    def __init__(self, request_scope: UserAndDatabaseConnection):
         super().__init__(
             RepositoryDependencies(
-                db, Entity.USER_CONTACT_INFORMATION.value, entity_models
+                request_scope.initiating_user_id,
+                request_scope.db,
+                Entity.COVER_LETTERS.value,
+                entity_models,
             ),
             required_parent_keys=[Entity.USERS.value],
         )
```

### Comparing `getajob-0.3.5/getajob/contexts/users/demographics/models.py` & `getajob-0.4.0/getajob/contexts/users/demographics/models.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/contexts/users/demographics/repository.py` & `getajob-0.4.0/getajob/contexts/users/qualifications/repository.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,23 +1,28 @@
 from getajob.vendor.firestore.repository import FirestoreDB
 from getajob.abstractions.repository import (
     SingleChildRepository,
     RepositoryDependencies,
 )
-from getajob.abstractions.models import Entity, EntityModels
+from getajob.abstractions.models import Entity, EntityModels, UserAndDatabaseConnection
 
-from .models import UserDemographicData, DemographicData
+from .models import Qualifications, UserQualifications
 
 
 entity_models = EntityModels(
-    entity=UserDemographicData,
-    create=DemographicData,
-    update=DemographicData,
+    entity=UserQualifications,
+    create=Qualifications,
+    update=Qualifications,
 )
 
 
-class UserDemographicsRepository(SingleChildRepository):
-    def __init__(self, db: FirestoreDB):
+class UserQualificationsRepository(SingleChildRepository):
+    def __init__(self, request_scope: UserAndDatabaseConnection):
         super().__init__(
-            RepositoryDependencies(db, Entity.USER_DEMOGRAPHICS.value, entity_models),
+            RepositoryDependencies(
+                request_scope.initiating_user_id,
+                request_scope.db,
+                Entity.USER_QUALIFICATIONS.value,
+                entity_models,
+            ),
             required_parent_keys=[Entity.USERS.value],
         )
```

### Comparing `getajob-0.3.5/getajob/contexts/users/job_preferences/models.py` & `getajob-0.4.0/getajob/contexts/users/job_preferences/models.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/contexts/users/job_preferences/repository.py` & `getajob-0.4.0/getajob/contexts/users/resumes/repository.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,25 +1,28 @@
 from getajob.vendor.firestore.repository import FirestoreDB
 from getajob.abstractions.repository import (
-    SingleChildRepository,
+    MultipleChildrenRepository,
     RepositoryDependencies,
 )
-from getajob.abstractions.models import Entity, EntityModels
+from getajob.abstractions.models import Entity, EntityModels, UserAndDatabaseConnection
 
-from .models import UserJobPreferences, JobPreferences
+from .models import Resume, CreateResume
 
 
 entity_models = EntityModels(
-    entity=UserJobPreferences,
-    create=JobPreferences,
-    update=JobPreferences,
+    entity=Resume,
+    create=CreateResume,
+    update=CreateResume,
 )
 
 
-class UserJobPreferencesRepository(SingleChildRepository):
-    def __init__(self, db: FirestoreDB):
+class ResumeRepository(MultipleChildrenRepository):
+    def __init__(self, request_scope: UserAndDatabaseConnection):
         super().__init__(
             RepositoryDependencies(
-                db, Entity.USER_JOB_PREFERENCES.value, entity_models
+                request_scope.initiating_user_id,
+                request_scope.db,
+                Entity.RESUMES.value,
+                entity_models,
             ),
             required_parent_keys=[Entity.USERS.value],
         )
```

### Comparing `getajob-0.3.5/getajob/contexts/users/qualifications/models.py` & `getajob-0.4.0/getajob/contexts/users/qualifications/models.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/exceptions.py` & `getajob-0.4.0/getajob/exceptions.py`

 * *Files 10% similar despite different names*

```diff
@@ -62,7 +62,12 @@
     def __init__(self):
         super().__init__("Kafka event topic must be provided")
 
 
 class MissingParentKeyError(Exception):
     def __init__(self, parent_key: str):
         super().__init__(f"Missing parent key: {parent_key}")
+
+
+class EntityDoesNotMatchError(Exception):
+    def __init__(self, entity_type: str):
+        super().__init__(f"{entity_type} Does not match")
```

### Comparing `getajob-0.3.5/getajob/test_support/fixtures/application.py` & `getajob-0.4.0/getajob/test_support/fixtures/application.py`

 * *Files 12% similar despite different names*

```diff
@@ -16,39 +16,42 @@
 from .job import JobFixture
 
 
 class ApplicationWithDependencies(BaseModel):
     application: Any
     company: Any
     job: Any
+    resume: Any
 
 
 class ApplicationFixture:
     @staticmethod
-    def create_application(db, user, resume, company, job):
-        application_repo = ApplicationRepository(db)
+    def create_application(request_scope, user, resume, company, job):
+        application_repo = ApplicationRepository(request_scope)
         new_application = application_repo.user_creates_application(
             user_id=user.id,
             application=UserCreatedApplication(
                 company_id=company.id, job_id=job.id, resume_id=resume.id
             ),
         )
         new_application = cast(Application, new_application)
         return new_application
 
     @staticmethod
-    def create_application_with_dependencies(db):
-        user = cast(User, UserFixtures.create_user_from_webhook(db))
-        resume = cast(Resume, UserFixtures.create_user_resume(db, user.id))
-        company = cast(Company, CompanyFixture.create_company_from_webhook(db))
-        job = cast(Job, JobFixture.create_job(db, company.id))
-        application_repo = ApplicationRepository(db)
+    def create_application_with_dependencies(request_scope):
+        user = cast(User, UserFixtures.create_user_from_webhook(request_scope))
+        resume = cast(Resume, UserFixtures.create_user_resume(request_scope, user.id))
+        company = cast(
+            Company, CompanyFixture.create_company_from_webhook(request_scope)
+        )
+        job = cast(Job, JobFixture.create_job(request_scope, company.id))
+        application_repo = ApplicationRepository(request_scope)
         new_application = application_repo.user_creates_application(
             user_id=user.id,
             application=UserCreatedApplication(
                 company_id=company.id, job_id=job.id, resume_id=resume.id
             ),
         )
         new_application = cast(Application, new_application)
         return ApplicationWithDependencies(
-            application=new_application, company=company, job=job
+            application=new_application, company=company, job=job, resume=resume
         )
```

### Comparing `getajob-0.3.5/getajob/test_support/fixtures/company.py` & `getajob-0.4.0/getajob/test_support/fixtures/company.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from getajob.vendor.clerk.companies.repository import WebhookCompanyRepository
 from getajob.vendor.clerk.companies.models import ClerkCompanyWebhookEvent
 
 
 class CompanyFixture:
     @staticmethod
-    def create_company_from_webhook(db):
+    def create_company_from_webhook(request_scope):
         data = {
             "data": {
                 "created_at": 1654013202977,
                 "created_by": "user_1vq84bqWzw7qmFgqSwN4CH1Wp0n",
                 "id": "org_29w9IfBrPmcpi0IeBVaKtA7R94W",
                 "image_url": "https://img.clerk.com/xxxxxx",
                 "logo_url": "https://example.org/example.png",
@@ -18,9 +18,9 @@
                 "slug": "acme-inc",
                 "updated_at": 1654013202977,
             },
             "object": "event",
             "type": "organization.created",
         }
         company = ClerkCompanyWebhookEvent(**data)
-        repo = WebhookCompanyRepository(db)
+        repo = WebhookCompanyRepository(request_scope)
         return repo.create_company(company)
```

### Comparing `getajob-0.3.5/getajob/test_support/fixtures/recruiter_invitation.py` & `getajob-0.4.0/getajob/test_support/fixtures/recruiter_invitation.py`

 * *Files 12% similar despite different names*

```diff
@@ -6,13 +6,13 @@
 from getajob.vendor.clerk.recruiter_invitation.models import (
     ClerkCompanyInvitationsWebhookEvent,
 )
 
 
 class RecruiterInvitationFixture:
     @staticmethod
-    def create_recruiter_invitation_from_webhook(db):
+    def create_recruiter_invitation_from_webhook(request_scope):
         with open("tests/mocks/webhooks/create_recruiter_invitation.json", "r") as f:
             data = json.load(f)
         invitation = ClerkCompanyInvitationsWebhookEvent(**data)
-        repo = WebhookCompanyInvitationRepository(db)
+        repo = WebhookCompanyInvitationRepository(request_scope)
         return repo.create_invitation(invitation)
```

### Comparing `getajob-0.3.5/getajob/test_support/fixtures/scheduled_events.py` & `getajob-0.4.0/getajob/test_support/fixtures/scheduled_events.py`

 * *Files 12% similar despite different names*

```diff
@@ -6,15 +6,15 @@
     CreateScheduledEvent,
 )
 from getajob.contexts.scheduled_events.enumerations import ReportScheduledEvent
 
 
 class ScheduledEventsFixture:
     @staticmethod
-    def create_scheduled_events(db):
+    def create_scheduled_events(request_scope):
         event_1 = CreateScheduledEvent(
             related_object_id="test",
             name="Test Event",
             description="Test Description",
             cron="* * * * *",
             event_category=ScheduledEventCategory.REPORT,
             event_type=ReportScheduledEvent.APPLICANT_SUMMARY,
@@ -34,11 +34,11 @@
             name="Test Event 3",
             description="Test Description 3",
             cron="* * * * *",
             event_category=ScheduledEventCategory.REPORT,
             event_type=ReportScheduledEvent.APPLICANT_SUMMARY,
             next_run_time=datetime.utcnow() + timedelta(days=1),
         )
-        repo = ScheduledEventsRepository(db)
+        repo = ScheduledEventsRepository(request_scope)
         repo.create(event_1)
         repo.create(event_2)
         repo.create(event_3)
```

### Comparing `getajob-0.3.5/getajob/test_support/fixtures/users.py` & `getajob-0.4.0/getajob/test_support/fixtures/users.py`

 * *Files 8% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 from getajob.vendor.clerk.users.models import ClerkUserWebhookEvent
 from getajob.contexts.users.resumes.repository import ResumeRepository
 from getajob.contexts.users.resumes.models import CreateResume
 
 
 class UserFixtures:
     @staticmethod
-    def create_user_from_webhook(db):
+    def create_user_from_webhook(request_scope):
         data = {
             "data": {
                 "birthday": "",
                 "created_at": 1654012591514,
                 "email_addresses": [
                     {
                         "email_address": "example@example.org",
@@ -44,17 +44,17 @@
                 "username": None,
                 "web3_wallets": [],
             },
             "object": "event",
             "type": "user.created",
         }
         user = ClerkUserWebhookEvent(**data)
-        repo = WebhookUserRepository(db)
+        repo = WebhookUserRepository(request_scope)
         return repo.create_user(user)
 
     @staticmethod
-    def create_user_resume(db, user_id: str):
-        repo = ResumeRepository(db)
+    def create_user_resume(request_scope, user_id: str):
+        repo = ResumeRepository(request_scope)
         return repo.create(
             data=CreateResume(resume="nice resume"),
             parent_collections={Entity.USERS.value: user_id},
         )
```

### Comparing `getajob-0.3.5/getajob/vendor/algolia/models.py` & `getajob-0.4.0/getajob/vendor/algolia/models.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/clerk/client.py` & `getajob-0.4.0/getajob/vendor/clerk/client.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/clerk/companies/models.py` & `getajob-0.4.0/getajob/vendor/clerk/companies/models.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/clerk/companies/repository.py` & `getajob-0.4.0/getajob/vendor/clerk/companies/repository.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,38 +1,44 @@
 import typing as t
 
-from getajob.vendor.firestore.repository import FirestoreDB
 from getajob.vendor.kafka.repository import KafkaProducerRepository
 from getajob.vendor.kafka.models import KafkaEventConfig, KafkaTopic
 from getajob.abstractions.repository import ParentRepository, RepositoryDependencies
-from getajob.abstractions.models import Entity, EntityModels
+from getajob.abstractions.models import Entity, EntityModels, UserAndDatabaseConnection
 
 from .models import (
     ClerkCompanyWebhookEvent,
     ClerkCompany,
     ClerkCompanyDeleted,
     ClerkCompanyWebhookType,
 )
 
 entity_models = EntityModels(entity=ClerkCompany)
 
 
 class WebhookCompanyRepository(ParentRepository):
     def __init__(
-        self, db: FirestoreDB, kafka: t.Optional[KafkaProducerRepository] = None
+        self,
+        request_scope: UserAndDatabaseConnection,
+        kafka: t.Optional[KafkaProducerRepository] = None,
     ):
         kafka_event_config = KafkaEventConfig(
             topic=KafkaTopic.companies,
             create=True,
             update=True,
             delete=True,
         )
         super().__init__(
             RepositoryDependencies(
-                db, Entity.COMPANIES.value, entity_models, kafka, kafka_event_config
+                request_scope.initiating_user_id,
+                request_scope.db,
+                Entity.COMPANIES.value,
+                entity_models,
+                kafka,
+                kafka_event_config,
             )
         )
 
     def handle_webhook_event(self, event: ClerkCompanyWebhookEvent):
         event_dict = {
             ClerkCompanyWebhookType.organization_created: self.create_company,
             ClerkCompanyWebhookType.organization_updated: self.update_company,
```

### Comparing `getajob-0.3.5/getajob/vendor/clerk/mock.py` & `getajob-0.4.0/getajob/vendor/clerk/mock.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/clerk/recruiter_invitation/models.py` & `getajob-0.4.0/getajob/vendor/clerk/recruiter_invitation/models.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/clerk/recruiter_invitation/repository.py` & `getajob-0.4.0/getajob/vendor/clerk/recruiter_invitation/repository.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,25 +1,24 @@
-from getajob.vendor.firestore.repository import FirestoreDB
 from getajob.contexts.companies.invitations.repository import (
     RecruiterInvitationsRepository,
 )
-from getajob.abstractions.models import Entity, EntityModels
+from getajob.abstractions.models import Entity, EntityModels, UserAndDatabaseConnection
 
 from .models import (
     ClerkCompanyInvitation,
     ClerkCompanyInvitationsWebhookEvent,
     ClerkCompanyInvitationsWebhookType,
 )
 
 entity_models = EntityModels(entity=ClerkCompanyInvitation)
 
 
 class WebhookCompanyInvitationRepository:
-    def __init__(self, db: FirestoreDB):
-        self.repo = RecruiterInvitationsRepository(db)
+    def __init__(self, request_scope: UserAndDatabaseConnection):
+        self.repo = RecruiterInvitationsRepository(request_scope)
 
     def handle_webhook_event(self, event: ClerkCompanyInvitationsWebhookEvent):
         event_dict = {
             ClerkCompanyInvitationsWebhookType.organization_invitation_created: self.create_invitation,
             ClerkCompanyInvitationsWebhookType.organization_invitation_revoked: self.revoke_invitation,
             ClerkCompanyInvitationsWebhookType.organization_invitation_accepted: self.accept_invitation,
         }
```

### Comparing `getajob-0.3.5/getajob/vendor/clerk/recruiters/models.py` & `getajob-0.4.0/getajob/vendor/clerk/recruiters/models.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/clerk/recruiters/repository.py` & `getajob-0.4.0/getajob/vendor/clerk/recruiters/repository.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,9 +1,8 @@
-from getajob.vendor.firestore.repository import FirestoreDB
-from getajob.abstractions.models import Entity, EntityModels
+from getajob.abstractions.models import Entity, EntityModels, UserAndDatabaseConnection
 from getajob.contexts.companies.recruiters.repository import RecruiterRepository
 
 
 from .models import (
     ClerkCompanyMembershipWebhookEvent,
     ClerkCompanyMembership,
     ClerkCompanyMembershipWebhookType,
@@ -12,19 +11,16 @@
     UpdateClerkCompanyMemberWithRole,
 )
 
 entity_models = EntityModels(entity=ClerkCompanyMember)
 
 
 class WebhookCompanyMembershipRepository:
-    def __init__(
-        self,
-        db: FirestoreDB,
-    ):
-        self.repo = RecruiterRepository(db)
+    def __init__(self, request_scope: UserAndDatabaseConnection):
+        self.repo = RecruiterRepository(request_scope)
 
     def handle_webhook_event(self, event: ClerkCompanyMembershipWebhookEvent):
         event_dict = {
             ClerkCompanyMembershipWebhookType.organization_membership_created: self.create_recruiter,
             ClerkCompanyMembershipWebhookType.organization_membership_updated: self.update_recruiter,
             ClerkCompanyMembershipWebhookType.organization_membership_deleted: self.delete_recruiter,
         }
```

### Comparing `getajob-0.3.5/getajob/vendor/clerk/repository.py` & `getajob-0.4.0/getajob/vendor/clerk/repository.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/clerk/users/models.py` & `getajob-0.4.0/getajob/vendor/clerk/users/models.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/clerk/users/repository.py` & `getajob-0.4.0/getajob/vendor/clerk/users/repository.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,39 +1,45 @@
 import typing as t
 
-from getajob.vendor.firestore.repository import FirestoreDB
 from getajob.vendor.kafka.repository import KafkaProducerRepository
 from getajob.vendor.kafka.models import KafkaEventConfig, KafkaTopic
 from getajob.abstractions.repository import ParentRepository, RepositoryDependencies
-from getajob.abstractions.models import Entity, EntityModels
+from getajob.abstractions.models import Entity, EntityModels, UserAndDatabaseConnection
 
 from .models import (
     ClerkUser,
     ClerkUserWebhookEvent,
     ClerkUserWebhookType,
     ClerkWebhookUserDeleted,
     ClerkWebhookUserUpdated,
 )
 
 entity_models = EntityModels(entity=ClerkUser, update=ClerkWebhookUserUpdated)
 
 
 class WebhookUserRepository(ParentRepository):
     def __init__(
-        self, db: FirestoreDB, kafka: t.Optional[KafkaProducerRepository] = None
+        self,
+        request_scope: UserAndDatabaseConnection,
+        kafka: t.Optional[KafkaProducerRepository] = None,
     ):
         kafka_event_config = KafkaEventConfig(
             topic=KafkaTopic.users,
             create=True,
             update=True,
             delete=True,
         )
         super().__init__(
             RepositoryDependencies(
-                db, Entity.USERS.value, entity_models, kafka, kafka_event_config
+                request_scope.initiating_user_id,
+                request_scope.db,
+                Entity.USERS.value,
+                entity_models,
+                kafka,
+                kafka_event_config,
             )
         )
 
     def handle_webhook_event(self, event: ClerkUserWebhookEvent):
         event_dict = {
             ClerkUserWebhookType.user_created: self.create_user,
             ClerkUserWebhookType.user_updated: self.update_user,
```

### Comparing `getajob-0.3.5/getajob/vendor/firestore/client_factory.py` & `getajob-0.4.0/getajob/vendor/firestore/client_factory.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/firestore/helpers.py` & `getajob-0.4.0/getajob/vendor/firestore/helpers.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/firestore/models.py` & `getajob-0.4.0/getajob/vendor/firestore/models.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/firestore/repository.py` & `getajob-0.4.0/getajob/vendor/firestore/repository.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/kafka/authentication.py` & `getajob-0.4.0/getajob/vendor/kafka/authentication.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/kafka/client_factory.py` & `getajob-0.4.0/getajob/vendor/kafka/client_factory.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/kafka/mock.py` & `getajob-0.4.0/getajob/vendor/kafka/mock.py`

 * *Files 10% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 class MockKafkaProducer(KafkaProducer):
     # pylint: disable=super-init-not-called
     def __init__(self, *args, **kwargs):
         self.message_count = 0
 
     def send(self, *args, **kwargs):
         self.message_count += 1
+        print("SENDING MESSAGE", args, kwargs)
 
     def flush(self, *args, **kwargs):
         ...
 
     def close(self, *args, **kwargs):
         ...
```

### Comparing `getajob-0.3.5/getajob/vendor/kafka/repository.py` & `getajob-0.4.0/getajob/vendor/kafka/repository.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/openai/mock.py` & `getajob-0.4.0/getajob/vendor/openai/mock.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/openai/repository.py` & `getajob-0.4.0/getajob/vendor/openai/repository.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/getajob/vendor/openai/settings.py` & `getajob-0.4.0/getajob/vendor/openai/settings.py`

 * *Files identical despite different names*

### Comparing `getajob-0.3.5/pyproject.toml` & `getajob-0.4.0/pyproject.toml`

 * *Files 15% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "getajob"
-version = "0.3.5"
+version = "0.4.0"
 description = ""
 authors = ["Your Name <you@example.com>"]
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.11"
 aiohttp = "3.8.4"
@@ -70,12 +70,13 @@
 wrapt = "1.15.0"
 yarl = "1.9.2"
 sendgrid = "6.10.0"
 fastapi = "0.95.2"
 sentry-sdk = {extras = ["fastapi"], version = "^1.25.0"}
 aiocron = "^1.8"
 mock-firestore = "^0.11.0"
+redis = "^4.6.0"
 
 
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `getajob-0.3.5/PKG-INFO` & `getajob-0.4.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: getajob
-Version: 0.3.5
+Version: 0.4.0
 Summary: 
 Author: Your Name
 Author-email: you@example.com
 Requires-Python: >=3.11,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: aiocron (>=1.8,<2.0)
@@ -55,14 +55,15 @@
 Requires-Dist: pyasn1-modules (==0.3.0)
 Requires-Dist: pycparser (==2.21)
 Requires-Dist: pydantic (==1.10.8)
 Requires-Dist: pyjwt (==2.7.0)
 Requires-Dist: pyparsing (==3.0.9)
 Requires-Dist: python-dateutil (==2.8.2)
 Requires-Dist: python-dotenv (==1.0.0)
+Requires-Dist: redis (>=4.6.0,<5.0.0)
 Requires-Dist: requests (==2.31.0)
 Requires-Dist: rsa (==4.9)
 Requires-Dist: sendgrid (==6.10.0)
 Requires-Dist: sentry-sdk[fastapi] (>=1.25.0,<2.0.0)
 Requires-Dist: six (==1.16.0)
 Requires-Dist: sniffio (==1.3.0)
 Requires-Dist: svix (==0.85.1)
```

