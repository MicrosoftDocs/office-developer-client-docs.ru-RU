---
title: Макрокоманда StopAllMacros
TOCTitle: StopAllMacros macro action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4e44182dd4290b05a2cfc8fabdf9240819f4b7aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314478"
---
# <a name="stopallmacros-macro-action"></a>Макрокоманда StopAllMacros


**Область применения**: Access 2013, Office 2013

Действие **StopAllMacros** можно использовать для остановки всех запущенных макросов.

## <a name="setting"></a>Setting

Действие **StopAllMacros** не имеет аргументов.

## <a name="remarks"></a>Заметки

Обычно это действие используется, когда из-за ошибки необходимо остановить все макрос. В строке действий макроса можно использовать условное выражение, которое содержит это действие. Если выражение имеет  true (–1), Microsoft Access останавливает все макрос.

Например, у вас может быть макрос, который отображает окно сообщения как одно из нескольких сложных действий, включая запуск других макроса. Если пользователь нажмет кнопку **"Отмена"** в этом окне сообщения, действие **StopAllMacros** может остановить все запущенные макрос.

Если макрос использовал действия **Echo** или **SetWarnings** для выключения эха или отображения системных сообщений, действие **StopAllMacros** автоматически включает их.

Это действие не доступно в модуле Visual Basic для приложений VBA.

