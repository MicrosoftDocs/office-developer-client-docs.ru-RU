---
title: CloseDatabase Macro Action
TOCTitle: CloseDatabase Macro Action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2c60d53b6798d3385bdcfb17669134a04ba6195
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483091"
---
# <a name="closedatabase-macro-action"></a>CloseDatabase Macro Action


**Применимо к**: Access 2013 | Office 2013

Действие **CloseDatabase** можно использовать для закрытия текущей базы данных.

## <a name="setting"></a>Параметр

Действие **CloseDatabase** не имеет каких-либо аргументов.

## <a name="remarks"></a>Замечания

  - Access не будут запускаться все действия, которые выполните действие **CloseDatabase** в макросе.

  - Это действие имеет тот же эффект, как на вкладку **файл** и выбрав команду **Закрыть базы данных**. При наличии несохраненных объектов открыть при запуске действия **CloseDatabase** , диалоговых окон, которые отображаются такие же, как, отображаемые при нажатии кнопки **Закрыть базы данных**.

  - Чтобы выполнить действие **CloseDatabase** в Visual Basic для приложений (VBA) модуль, используйте метод **CloseDatabase** **объекта** .

