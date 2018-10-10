---
title: 'Chapter 9: Data Shaping'
TOCTitle: 'Chapter 9: Data Shaping'
ms:assetid: f66a319f-1b3d-c4a3-50b3-af1a47540832
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250253(v=office.15)
ms:contentKeyID: 48548739
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8217be1004ea8304501e7d32908b8af269873b7a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482290"
---
# <a name="chapter-9-data-shaping"></a>Chapter 9: Data Shaping


**Применимо к**: Access 2013 | Office 2013

*Формирование данных* предоставляет способ для запроса источника данных и возврата [набора записей](recordset-object-ado.md) , представляющий отношение родитель потомок между двумя или более логические сущности (иерархии). Классический пример иерархической связи — клиентов и заказы. Для каждого клиента в базе данных может быть ноль или больше заказов. Регулярные SQL предоставляет средства извлечения данных, с помощью синтаксиса, но это может быть неэффективны и громоздким, так как избыточных родительских данных повторяется в каждой записи возвращаются для связь с заданным родитель потомок. Формирование данных можно связать один родительской записи в родительском **записей** несколько дочерних записей в дочерних **записей**, избегая избыточность соединения. Большинство пользователей поиск родитель потомок нескольких **записей** модель программирования более естественный и более удобен для работы с более одной модели ОБЪЕДИНЕНИЯ **набора записей** .

Также формирования синтаксис данных предоставляет другие возможности. Разработчики могут создавать новые объекты **набора записей** без источника данных с помощью ключевого слова NEW для описания полей родительских и дочерних **наборов записей**. Новый объект **набора записей** можно заполненный данными и постоянно хранятся. Разработчики также можно выполнить различные вычисления или aggregations (например, сумм, AVG и максимальное число) на подчиненные поля. Формирование данных также можно создавать родительского **набора записей** из дочерних **записей** группировки записей в дочернем и поместить одну строку в родительской для каждой группы в дочернем.

В следующих разделах для получения дополнительных сведений о формирования данных:

  - [Data Shaping Summary](data-shaping-summary.md)

  - [Required Providers for Data Shaping](required-providers-for-data-shaping.md)

  - [Shape Commands in General](shape-commands-in-general.md)

  - [Предложение APPEND фигуры](shape-append-clause.md)

  - [Предложение COMPUTE фигуры](shape-compute-clause.md)

  - [Fabricating Hierarchical Recordsets](fabricating-hierarchical-recordsets.md)

  - [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md)

  - [Formal Shape Grammar](formal-shape-grammar.md)

  - [Visual Basic для приложений функции](visual-basic-for-applications-functions.md)

