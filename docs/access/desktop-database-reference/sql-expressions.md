---
title: Выражения SQL (Справочник по для настольных баз данных Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25b7d11430b730b6cedd1d8a084acd4984c5f292
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944153"
---
# <a name="sql-expressions"></a>Выражения SQL


**Применимо к**: Access 2013, Office 2013

Выражение SQL — это строка, которая значительно облегчает копирование полностью или частично инструкции SQL. Например метод**FindFirst** **целиком** использует выражение SQL, составляет выбора SQL [предложение WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)).

Ядро базы данных Microsoft Access используется служба выражений Microsoft Visual Basic для приложений (или VBA) для выполнения простых вычислений арифметические операторы и функции. Все операторы, используемые в выражения SQL ядра базы данных Microsoft Access (за исключением **[ **[между](https://msdn.microsoft.com/library/ff192436\(v=office.15\))** и **[как](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**)](https://msdn.microsoft.com/library/ff836369\(v=office.15\))** определены службы выражений VBA. Кроме того, VBA выражения, которые предлагает служба более 100 функций, которые можно использовать в выражениях SQL. Например эти функции VBA можно использовать для создания запроса SQL в режиме конструктора запроса Microsoft Access, и можно также использовать эти функции в SQL-запроса в методе DAO **OpenRecordset** в Microsoft Visual C++, Microsoft Visual Basic и Microsoft Код Excel.

