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
# <a name="using-addnew-in-immediate-and-batch-modes"></a>Использование AddNew в немедленных и пакетных режимах


**Область применения**: Access 2013, Office 2013

Поведение метода **AddNew** зависит от режима обновления объекта **Recordset** и от того, передаются ли аргументы *FieldList* и *Values.*

В режиме немедленного обновления (в котором поставщик записывает изменения в исходный источник данных после вызова метода **Update),** вызов метода **AddNew** без аргументов задает для свойства **EditMode** свойство **adEditAdd.** Поставщик кэшетет все изменения значения поля локально. Вызов метода **Update** публикует новую запись в базе данных и сбрасывает свойство **EditMode** в **adEditNone.** Если передать *аргументы FieldList* и *Values,* ADO немедленно публикует новую запись в базе данных (вызов **обновления** не требуется); Значение **свойства EditMode** не меняется (**adEditNone).**

В режиме пакетного обновления вызов метода **AddNew** без аргументов задает для свойства **EditMode** **свойство adEditAdd.** Поставщик кэшетет все изменения значения поля локально. Вызов метода **Update** добавляет новую запись в текущий набор **recordset** и сбрасывает свойство **EditMode** в **adEditNone,** но поставщик не записи изменений в баз данных, пока вы не вызываете **метод UpdateBatch.** Если передать *аргументы FieldList* и *Values,* ADO отправляет новую запись поставщику для хранения в кэше; Необходимо вызвать метод **UpdateBatch,** чтобы опубликовать новую запись в базовую базу данных. Дополнительные сведения об **обновлении** и **UpdateBatch** см. в главе [5 "Обновление и сохраняемая информация".](chapter-5-updating-and-persisting-data.md)

