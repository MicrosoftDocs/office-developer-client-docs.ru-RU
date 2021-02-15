---
title: Динамическое свойство Prompt (ADO)
TOCTitle: Prompt dynamic property (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 261ac5640b5239f27ad91e01d1cb23794f88740a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301325"
---
# <a name="prompt-dynamic-property-ado"></a>Динамическое свойство Prompt (ADO)

**Область применения**: Access 2013, Office 2013

Указывает, должен ли поставщик OLE DB затметь пользователю информацию об инициализации.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает и возвращает значение [ConnectPromptEnum.](connectpromptenum.md)

## <a name="remarks"></a>Заметки

**Prompt** — это динамическое свойство, которое поставщик [OLE](properties-collection-ado.md) DB может быть примечен к коллекции свойств объекта [Connection.](connection-object-ado.md) Для запроса сведений об инициализации поставщики OLE DB обычно отображают пользователю диалоговое окно.

Динамические свойства объекта [Connection](connection-object-ado.md) теряются при закрытии **подключения.** Перед **повторной** открытием подключения необходимо сбросить свойство **Prompt,** чтобы использовать значение, не используемого по умолчанию.

> [!NOTE]
> Не следует указывать, что поставщик должен затметь пользователя в сценариях, в которых пользователь не сможет ответить на диалоговое окно. Например, пользователь не сможет ответить, если приложение запущено в серверной системе, а не в клиенте пользователя, или если приложение запущено в системе без входа пользователя. В таких случаях приложение будет ждать ответа неопределенное время и, кажется, блокируется.

**Использование**

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
