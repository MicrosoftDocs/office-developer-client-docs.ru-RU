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

Вы можете использовать действие **Макрокоманда stopallmacros** , чтобы остановить все выполняемые в данный момент макросы.

## <a name="setting"></a>Параметр

Макрокоманда **Макрокоманда stopallmacros** не содержит аргументов.

## <a name="remarks"></a>Примечания

Обычно это действие используется, когда условие ошибки делает необходимо остановить все макросы. В строке действий макроса, содержащей это действие, можно использовать условное выражение. Если выражение имеет **значение true** (– 1), Microsoft Access прекратит выполнение всех макросов.

Например, у вас может быть макрос, отображающий окно сообщения в виде одного из нескольких сложных действий, в том числе выполнение других макросов. Если пользователь нажимает кнопку **Cancel (Отмена** ) в этом окне сообщения, действие **Макрокоманда stopallmacros** может остановить все запущенные макросы.

Если в макросе используются действия **echo** или **сетварнингс** для отключения эхо или отображения системных сообщений, действие **Макрокоманда stopallmacros** автоматически включает их снова.

Это действие недоступно в модуле Visual Basic для приложений (VBA).

