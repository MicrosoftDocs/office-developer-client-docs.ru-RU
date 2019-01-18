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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714439"
---
# <a name="closedatabase-macro-action"></a>Макрокоманда CloseDatabase


**Применимо к**: Access 2013, Office 2013

Действие **CloseDatabase** можно использовать для закрытия текущей базы данных.

## <a name="setting"></a>Setting

Действие **CloseDatabase** не имеет каких-либо аргументов.

## <a name="remarks"></a>Замечания

  - Access не будут запускаться все действия, которые выполните действие **CloseDatabase** в макросе.

  - Это действие имеет тот же эффект, как на вкладку **файл** и выбрав команду **Закрыть базы данных**. При наличии несохраненных объектов открыть при запуске действия **CloseDatabase** , диалоговых окон, которые отображаются такие же, как, отображаемые при нажатии кнопки **Закрыть базы данных**.

  - Чтобы выполнить действие **CloseDatabase** в Visual Basic для приложений (VBA) модуль, используйте метод **CloseDatabase** **объекта** .

