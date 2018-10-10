---
title: Using AddNew in Immediate and Batch Modes
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b37acc1819d12acc1e659be85361c3c09b84ebdb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480803"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a>Using AddNew in Immediate and Batch Modes


**Применимо к**: Access 2013 | Office 2013

Поведение метода **AddNew** зависит от режима обновления объекта **набора записей** и ли передавать аргументы *FieldList* и их *значения* .

В режиме немедленное обновление (где поставщик записывает изменения к базовому источнику данных после вызова метода **Update** ) вызов метода **AddNew** без аргументов присваивает свойству **EditMode** значение **adEditAdd.** Поставщик кэширует изменения значений полей локально. Вызов метода **Update** публикует новую запись в базу данных и сбрасывает свойство **EditMode** **как таковые**. Если передать аргументы *FieldList* и *значения* , ADO немедленно публикует новую запись в базу данных (без вызова **обновления** не требуется); значение свойства **EditMode** не изменяется (**как таковые**).

Вызов метода **AddNew** без аргументов в пакетном режиме обновления, присваивает свойству **EditMode** **adEditAdd**. Поставщик кэширует изменения значений полей локально. Вызов метода **Update** добавляет новую запись текущего **набора записей** и сбрасывает свойство **EditMode** **как таковые**, но поставщик не учесть изменения в основной базе данных, пока не будет вызван **UpdateBatch **метод. Если передать аргументы *FieldList* и *значения* , ADO отправляет новую запись поставщика для хранения в кэше; необходимо вызвать метод **UpdateBatch** для публикации новой записи в основной базе данных. Дополнительные сведения об **обновлении** и **UpdateBatch**можно [Глава 5: обновления и сохранение данных](chapter-5-updating-and-persisting-data.md).

