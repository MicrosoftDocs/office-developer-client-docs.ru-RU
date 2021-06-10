---
title: Using AddNew in Immediate and Batch Modes
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 929c01032924182d8db1bd5b06b573fb5d0171ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312756"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a>Использование AddNew в режимах Immediate и Batch


**Область применения**: Access 2013, Office 2013

Поведение метода **AddNew** зависит от режима обновления объекта **Recordset** и от того, передаете ли вы аргументы *FieldList* и *Values.*

В режиме немедленного обновления (в котором поставщик записывает изменения  в исходный источник данных после вызова метода Update), вызов метода **AddNew** без аргументов задает свойство **EditMode** **adEditAdd.** Поставщик кэшет любых изменений локального значения поля. Вызов метода **Update** публикует новую запись в базу данных и сбрасывает свойство **EditMode** в **adEditNone.** Если вы передаете *аргументы FieldList* и *Values,* ADO немедленно публикует новую запись в базу данных (вызов **обновления** не требуется); значение **свойства EditMode** не меняется **(adEditNone).**

В режиме пакетного обновления вызов **метода AddNew** без аргументов задает свойство **EditMode** **adEditAdd.** Поставщик кэшет любых изменений локального значения поля. Вызов метода **Update** добавляет новую запись в текущий набор **recordset** и сбрасывает свойство **EditMode** в **adEditNone,** но поставщик не вывешит изменения в баз данных, пока не будет вызывать метод **UpdateBatch.** Если вы передаете *аргументы FieldList* и *Values,* ADO отправляет новую запись поставщику для хранения в кэше; для публикации новой записи в баз данных необходимо вызвать метод **UpdateBatch.** Дополнительные сведения об **обновлении и** **обновленииBatch** см. в главе [5: Обновление и сохраняющихся данных.](chapter-5-updating-and-persisting-data.md)

