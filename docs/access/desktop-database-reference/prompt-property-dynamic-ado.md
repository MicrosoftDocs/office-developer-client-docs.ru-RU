---
title: Prompt Property--Dynamic (ADO)
TOCTitle: Prompt Property--Dynamic (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cb858186942ac026cbf3e1020c4ac658537093a5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483252"
---
# <a name="prompt-property--dynamic-ado"></a>Prompt Property--Dynamic (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает, следует ли поставщик OLE DB запрашивать у пользователя сведения инициализации.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает и возвращает значение [ConnectPromptEnum](connectpromptenum.md) .

## <a name="remarks"></a>Замечания

**Запрос** — это динамические свойства, которое может добавляться в коллекцию [свойств](properties-collection-ado.md) объект [подключения](connection-object-ado.md) поставщика OLE DB. Запрашивать сведения об инициализации, поставщики OLE DB обычно отображения диалогового окна для пользователя.

Динамические свойства объекта [подключения](connection-object-ado.md) не сохраняются при закрытии **подключения** . Свойство **приглашение** необходимо сбросить до повторного открытия **подключения** использовать значение, отличное от по умолчанию.


> [!NOTE]
> <P>Не указать, что поставщик должен запрашивать у пользователя в сценариях, в которых пользователь не будет отвечать на диалоговое окно. Например пользователь не будет отвечать, если приложение работает на сервере системы, а не на клиенте пользователя или приложения в системе с без пользователя. В таких случаях приложение неограниченное время ожидания ответа и показаться блокировка.</P>



**Использование**

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
