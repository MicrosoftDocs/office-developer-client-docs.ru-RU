---
title: Добавление записей (ссылка на настольные базы данных)
TOCTitle: Adding records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 268cd381cdeef11f2a6f351160d930e4b169cfbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280289"
---
# <a name="adding-records"></a>Добавление записей

**Область применения**: Access 2013, Office 2013

Используйте метод **AddNew** для создания и инициализации новой записи в существующем **Наборе записей.** Вы можете использовать метод **Supports** с **значением CursorOptionEnum** **adAddNew,** чтобы проверить, можно ли добавлять записи к текущему объекту **Recordset.**

После вызова метода **AddNew** новая запись становится текущей и остается текущей после вызова метода **Update.** Если объект **Recordset** не поддерживает закладки, возможно, вы не сможете получить доступ к новой записи после перемещения на другую запись. Поэтому в зависимости от типа курсора может потребоваться вызвать метод **Requery,** чтобы сделать новую запись доступной.

Если вы вызываете **AddNew** при редактировании текущей записи или при добавлении новой записи, ADO вызывает метод **Update,** чтобы сохранить все изменения, а затем создает новую запись.

В этой статье содержатся следующие разделы:

- [Добавление нескольких полей](adding-multiple-fields.md)
- [Определение режима редактирования](determining-edit-mode.md)
- [Использование AddNew в режимах Immediate и Batch](using-addnew-in-immediate-and-batch-modes.md)

