---
title: Макрокоманда CloseDatabase
TOCTitle: CloseDatabase macro action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac29cbdae8c162a992f2763530514150ca0240ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296299"
---
# <a name="closedatabase-macro-action"></a>Макрокоманда CloseDatabase


**Область применения**: Access 2013, Office 2013

Для закрытия текущей базы данных можно использовать действие **клоседатабасе** .

## <a name="setting"></a>Параметр

Действие **клоседатабасе** не имеет аргументов.

## <a name="remarks"></a>Примечания

  - Access не будет выполнять никакие действия, которые следуют за действием **клоседатабасе** в макросе.

  - Это действие эквивалентно нажатию вкладки **файл** и нажатию кнопки **Закрыть базу данных**. Если при выполнении действия **клоседатабасе** открыты несохраненные объекты, отображаются диалоговые окна, которые отображаются при нажатии кнопки **Закрыть базу данных**.

  - Чтобы запустить действие **клоседатабасе** в модуле Visual Basic для приложений (VBA), используйте метод **клоседатабасе** объекта **DoCmd** .

