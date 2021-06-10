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

Для закрытия текущей базы данных можно использовать действие **CloseDatabase.**

## <a name="setting"></a>Параметр

Действие **CloseDatabase** не имеет аргументов.

## <a name="remarks"></a>Примечания

  - Доступ не будет выполнять действия, которые следуют действию **CloseDatabase** в макросе.

  - Это действие имеет такой же эффект, как щелкнуть вкладку **Файл,** а затем нажать **закрыть базу данных**. Если при запуске действия **CloseDatabase** открываются какие-либо неоплаченные объекты, диалоговое окно, которое отображается, являются теми же, что и те, которые отображаются при нажатии кнопки **Закрыть базу данных.**

  - Чтобы выполнить действие **CloseDatabase** в модуле Visual Basic для приложений (VBA), используйте метод **CloseDatabase** объекта **DoCmd.**

