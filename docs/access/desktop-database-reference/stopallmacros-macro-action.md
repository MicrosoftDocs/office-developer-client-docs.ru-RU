---
title: StopAllMacros Macro Action
TOCTitle: StopAllMacros Macro Action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 80da04f7b5f99fd0b249164caaeaca9f25edd172
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479839"
---
# <a name="stopallmacros-macro-action"></a>StopAllMacros Macro Action


**Применимо к**: Access 2013 | Office 2013

Чтобы остановить все макросы, которые в настоящее время работает можно использовать действие **ОстановитьВсеМакросы** .

## <a name="setting"></a>Параметр

Действие **ОстановитьВсеМакросы** не требует аргументов.

## <a name="remarks"></a>Замечания

Это действие обычно используется для остановки всех макросов при ошибки. В строке действие макрос, содержащий это действие можно использовать условного выражения. Когда вычисление выражения дает значение **True** (– 1), Microsoft Access останавливает все макросы.

Например возможно, макрос, который отображает окно сообщения как один из нескольких сложных действий, включая выполнение других макросов. При нажатии кнопки **Отмена** сообщение, действие **ОстановитьВсеМакросы** можно остановить все макросы, на которых выполняется.

Если макрос **эхо** или **УстановитьСообщения** действий эхо или вывод системных сообщений, действие **ОстановитьВсеМакросы** автоматически включает их обратно.

Это действие недоступно в Visual Basic для приложений (VBA) модуля.

