---
title: 'Brief journey of sorting by specific custom order based on an association table values in PSQL'
excerpt: 'In this blog i will share how i manged to sort by custom order, for example i have a customers table with customer name, customer age, customer country name, address etc, i want to sort the users in a way that i want users from india first, america second, canada third, germany fourth assuming that i am only haveing customers from these countries. it would have been easy if i were to sort just in alphabeticall order or by age but its little diffrent approch i follwed here useing *case when* i did spent a day trying to figure out how to use this. The following query sorts in the order above mentioned'
coverImage: '/assets/blog/psql/cover.jpg'
date: '2022-11-03T05:35:07.322Z'
author:
  name: Jose KJ
  picture: '/assets/blog/authors/joe.jpeg'
ogImage:
  url: '/assets/blog/psql/cover.jpg'
---
In this blog i will share how i manged to sort by custom order, for example i have a customers table with customer name, customer age, customer country name, address etc, i want to sort the users in a way that i want users from india first, america second, canada third, germany fourth assuming that i am only haveing customers from these countries. it would have been easy if i were to sort just in alphabeticall order or by age but its little diffrent approch i follwed here useing *case when* i did spent a day trying to figure out how to use this. The following query sorts in the order above mentioned

select "name", "age", "country" from "customers"
order by
case "country" when
    'india' then 1,
    'america' then 2,
    'canada' then 3
    'germany' then 4
end limit 100;

## References:

1. https://dba.stackexchange.com/a/274389/263264

