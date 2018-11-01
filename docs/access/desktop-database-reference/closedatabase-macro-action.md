---
title: Действия макроса CloseDatabase
TOCTitle: CloseDatabase Macro Action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 42ba5925c35081f612bd4a81b49f3c2b16cf61dd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876640"
---
# <a name="closedatabase-macro-action"></a>Действия макроса CloseDatabase


**Применимо к**: Access 2013, Office 2013

Действие **CloseDatabase** можно использовать для закрытия текущей базы данных.

## <a name="setting"></a>Параметр

Действие **CloseDatabase** не имеет каких-либо аргументов.

## <a name="remarks"></a>Замечания

  - Access не будут запускаться все действия, которые выполните действие **CloseDatabase** в макросе.

  - Это действие имеет тот же эффект, как на вкладку **файл** и выбрав команду **Закрыть базы данных**. При наличии несохраненных объектов открыть при запуске действия **CloseDatabase** , диалоговых окон, которые отображаются такие же, как, отображаемые при нажатии кнопки **Закрыть базы данных**.

  - Чтобы выполнить действие **CloseDatabase** в Visual Basic для приложений (VBA) модуль, используйте метод **CloseDatabase** **объекта** .

