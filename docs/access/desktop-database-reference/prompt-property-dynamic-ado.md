---
title: Запрашивать динамического свойства (ADO)
TOCTitle: Prompt dynamic property (ADO)
ms:assetid: 6c899b03-1d1f-a81f-dc17-7205a0230af9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249428(v=office.15)
ms:contentKeyID: 48545473
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 893dfc7b2dd8ee66dc586fc3f5e98807ca1284cb
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996785"
---
# <a name="prompt-dynamic-property-ado"></a>Запрашивать динамического свойства (ADO)

**Применимо к**: Access 2013, Office 2013

Указывает, следует ли поставщик OLE DB запрашивать у пользователя сведения инициализации.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает и возвращает значение [ConnectPromptEnum](connectpromptenum.md) .

## <a name="remarks"></a>Примечания

**Запрос** — это динамические свойства, которое может добавляться в коллекцию [свойств](properties-collection-ado.md) объект [подключения](connection-object-ado.md) поставщика OLE DB. Запрашивать сведения об инициализации, поставщики OLE DB обычно отображения диалогового окна для пользователя.

Динамические свойства объекта [подключения](connection-object-ado.md) не сохраняются при закрытии **подключения** . Свойство **приглашение** необходимо сбросить до повторного открытия **подключения** использовать значение, отличное от по умолчанию.

> [!NOTE]
> Не указать, что поставщик должен запрашивать у пользователя в сценариях, в которых пользователь не будет отвечать на диалоговое окно. Например пользователь не будет отвечать, если приложение работает на сервере системы, а не на клиенте пользователя или приложения в системе с без пользователя. В таких случаях приложение неограниченное время ожидания ответа и показаться блокировка.

**Использование**

```vb
    Set cn = New Connection
    cn.Provider = "SQLOLEDB"
    cn.Properties("Prompt") = adPromptNever    ' do not prompt the user
```
