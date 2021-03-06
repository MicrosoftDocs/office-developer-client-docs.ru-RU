---
title: Обновление данных (ссылка на настольные базы данных)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e6989468e23fc1c9c611eb091172822a6ffe938
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313569"
---
# <a name="updating-data"></a>Обновление данных


**Область применения**: Access 2013, Office 2013

Обновление поведения и функциональности во многом зависит от режима обновления (типа блокировки), типа курсора и расположения курсора.

Используйте метод **Update,** чтобы сохранить все изменения, внесенные в текущую запись объекта **Recordset** после вызова метода **AddNew** или после изменения каких-либо значений поля в существующей записи. Объект **Recordset** должен поддерживать обновления.

Если объект **Recordset поддерживает** пакетное обновление, можно кэшировать несколько изменений в одну или несколько записей локально до вызова метода **UpdateBatch.** При редактировании текущей записи или добавлении новой записи при вызове метода **UpdateBatch** ADO будет автоматически вызывать метод Update, чтобы сохранить все ожидающие изменения текущей записи перед передачей пакетных изменений поставщику. 

Текущая запись остается текущей после вызова методов **Update** или **UpdateBatch.**

В этой статье содержатся следующие разделы:

- [Режим немедленного обновления](immediate-mode.md)
- [Обработка транзакций](transaction-processing.md)
- [Пакетный режим (ADO)](batch-mode.md)

