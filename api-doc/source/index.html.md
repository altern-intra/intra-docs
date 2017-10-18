---
title: EPITECH Intranet API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the EPITECH Intranet API Reference ! This page should explain you everything you need to know about the differents endpoints available
Note that a [NodeJS module](https://github.com/altern-intra/intra-api) is developped in order to wrap this API in Javascript.

This project is part of the [altern-intra](https://github.com/altern-intra/) project.
# Authentication

> Basic request with curl:

```shell
curl "https://intra.epitech.eu/autologin-token/?format=json"
```
> Make sure to replace `autologin-token` with your API key.

As of 18/11/2017, the Intranet API now requires you to use the autologin-token in order to use the API.
The combo login/Unix pswd is not available anymore. You can get your autologin-token here [autologin-token](https://intra.epitech.eu/admin/autolog)

The intranet considers that every request with the parameter format=json is an API call, so a basic API call would be this:
`https://intra.epitech.eu/autologin-token/?format=json`


<aside class="notice">
You must replace <code>autologin-token</code> with your personal autologin-token key.
</aside>

# Planning

## Get All Planning

```shell
curl "https://intra.epitech.eu/autologin-token/planning/load/?format=json"```

> The above command returns JSON structured like this:

```json
[{
  "scolaryear": "2017",
  "codemodule": "B-CPE-100",
  "codeinstance": "LYN-1-1",
  "codeacti": "acti-253708",
  "codeevent": "event-268252",
  "semester": 1,
  "instance_location": "FR/LYN",
  "titlemodule": "B1 - Unix & C Lab Seminar (Part I)",
  "prof_inst": [{
    "type": "user",
    "login": "victor1.granger@epitech.eu",
    "title": "Victor GRANGER",
    "picture": "https://cdn.local.epitech.eu/userprofil/victor1.granger.bmp"
  }, {
    "type": "user",
    "login": "morgan1.juillard-mancino@epitech.eu",
    "title": "morgan1 juillard-mancino",
    "picture": "https://cdn.local.epitech.eu/userprofil/morgan1.juillard-mancino.bmp"
  }],
  "acti_title": "Kick-Off - C Pool Day 01",
  "num_event": 1,
  "start": "2017-10-02 09:00:00",
  "end": "2017-10-02 09:30:00",
  "total_students_registered": 63,
  "title": null,
  "type_title": "Kick-Off",
  "type_code": "class",
  "is_rdv": "0",
  "nb_hours": "00:30:00",
  "allowed_planning_start": "2017-10-02 09:00:00",
  "allowed_planning_end": "2017-10-02 09:30:00",
  "nb_group": 1,
  "nb_max_students_projet": null,
  "room": {
    "code": "FR/LYN/Panoramic/001-002-003-004",
    "type": "salle_machine",
    "seats": 220
  },
  "dates": null,
  "module_available": false,
  "module_registered": false,
  "past": true,
  "allow_register": false,
  "event_registered": false,
  "display": "0",
  "project": false,
  "rdv_group_registered": null,
  "rdv_indiv_registered": null,
  "allow_token": false,
  "register_student": true,
  "register_prof": false,
  "register_month": false,
  "in_more_than_one_month": false
}, {
  "scolaryear": "2017",
  "codemodule": "B-CPE-100",
  "codeinstance": "LYN-1-1",
  "codeacti": "acti-253707",
  "codeevent": "event-268253",
  "semester": 1,
  "instance_location": "FR/LYN",
  "titlemodule": "B1 - Unix & C Lab Seminar (Part I)",
  "prof_inst": [{
    "type": "user",
    "login": "victor1.granger@epitech.eu",
    "title": "Victor GRANGER",
    "picture": "https://cdn.local.epitech.eu/userprofil/victor1.granger.bmp"
  }, {
    "type": "user",
    "login": "morgan1.juillard-mancino@epitech.eu",
    "title": "morgan1 juillard-mancino",
    "picture": "https://cdn.local.epitech.eu/userprofil/morgan1.juillard-mancino.bmp"
  }],
  "acti_title": "C Pool Day 01",
  "num_event": 1,
  "start": "2017-10-02 09:00:00",
  "end": "2017-10-02 21:30:00",
  "total_students_registered": 179,
  "title": null,
  "type_title": "TP",
  "type_code": "tp",
  "is_rdv": "0",
  "nb_hours": "12:30:00",
  "allowed_planning_start": "2017-10-02 08:42:00",
  "allowed_planning_end": "2017-10-03 23:42:00",
  "nb_group": 1,
  "nb_max_students_projet": "1",
  "room": {
    "code": "FR/LYN/Panoramic/001-002-003-004",
    "type": "salle_machine",
    "seats": 220
  },
  "dates": null,
  "module_available": false,
  "module_registered": false,
  "past": true,
  "allow_register": false,
  "event_registered": false,
  "display": "0",
  "project": true,
  "rdv_group_registered": null,
  "rdv_indiv_registered": null,
  "allow_token": false,
  "register_student": true,
  "register_prof": false,
  "register_month": false,
  "in_more_than_one_month": false
}]
```

This endpoint retrieves planing information. Note that without any parameters, it will return ALL ACTIVITIES AND EVENTS, which can be quite heavy to handle

### HTTP Request

`GET https://intra.epitech.eu/autologin-token/planning/load/?format=json`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
start | empty | start date to fetch events. Use 'yyyy-mm-dd' format
end | true | end date to fetch events. Use 'yyyy-mm-dd' format
