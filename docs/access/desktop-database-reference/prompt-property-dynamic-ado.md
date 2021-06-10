---
title: Быстрое динамическое свойство (ADO)
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
# <a name="prompt-dynamic-property-ado"></a>Быстрое динамическое свойство (ADO)

**Область применения**: Access 2013, Office 2013

Указывает, должен ли поставщик OLE DB подсказыть пользователю сведения о инициализации.

## <a name="settings-and-return-values"></a>Параметры и значения возврата

Задает и возвращает значение [ConnectPromptEnum.](connectpromptenum.md)

## <a name="remarks"></a>Примечания

**Prompt** — это динамическое свойство, которое может быть приобщено к коллекции [свойств](properties-collection-ado.md) объекта [Подключения](connection-object-ado.md) поставщиком OLE DB. Чтобы получить сведения о инициализации, поставщики OLE DB обычно отображают диалоговое окно пользователю.

Динамические свойства объекта [Подключения](connection-object-ado.md) теряются при **закрытии** подключения. Свойство **Prompt** должно быть сброшено перед повторной открытием **подключения,** чтобы использовать значение, помимо значения по умолчанию.

> [!NOTE]
> Не укажите, что поставщик должен подсказать пользователю сценарии, в которых пользователь не сможет отвечать на диалоговое окно. Например, пользователь не сможет отвечать, если приложение работает на серверной системе, а не на клиенте пользователя, или если приложение работает в системе без входа пользователя. В этих случаях приложение будет ждать ответа на неопределенное время и, как представляется, блокируется.

**Использование**

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
