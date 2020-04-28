---
title: Добавление записей (Справочник по базам данных Access на компьютере)
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

Используйте метод **AddNew** для создания и инициализации новой записи в существующем объекте **Recordset**. Можно **использовать метод support** со значением **курсороптионенум** , равным **ададднев** , чтобы проверить, можно ли добавлять записи в текущий объект **Recordset** .

После вызова метода **AddNew** новая запись становится текущей и остается текущей после вызова метода **Update** . Если объект **Recordset** не поддерживает закладки, вы не сможете получить доступ к новой записи после того, как вы перейдете к другой записи. Таким образом, в зависимости от типа курсора может потребоваться вызвать метод **Requery** , чтобы сделать новую запись доступной.

При вызове **AddNew** при редактировании текущей записи или добавлении новой записи ADO вызывает метод **Update** , чтобы сохранить изменения, а затем создает новую запись.

В этой статье содержатся следующие разделы:

- [Добавление нескольких полей](adding-multiple-fields.md)
- [Определение режима правки](determining-edit-mode.md)
- [Использование AddNew в непосредственных и пакетных режимах](using-addnew-in-immediate-and-batch-modes.md)

