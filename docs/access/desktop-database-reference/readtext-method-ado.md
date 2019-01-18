---
title: Метод ReadText (ADO)
TOCTitle: ReadText method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 883f74c06da83a46f9ffd1c30861d796c04b5c74
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699935"
---
# <a name="readtext-method-ado"></a>Метод ReadText (ADO)

**Применимо к**: Access 2013, Office 2013

Число операций чтения указанное число символов из объекта [потока](stream-object-ado.md) текста.

## <a name="syntax"></a>Синтаксис

*Строка* = *потока*. ReadText (*NumChars*)

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*NumChars* |Необязательно. **Длинное целое** значение, задающее число символов для чтения из файла, или значение [StreamReadEnum](streamreadenum.md) . Значение по умолчанию — **adReadAll**.|

## <a name="return-value"></a>Возвращаемое значение

Метод **ReadText** считывает указанное число символов, строку целиком или всей потока из объекта **потока** и возвращает результирующую строку.

## <a name="remarks"></a>Замечания

Если *NumChar* больше, чем количество символов в потоке, возвращаются только оставшиеся символы. Чтение строки не дополняется в соответствии с *NumChar*заданной длины. Если не используются никакие символы для чтения, возвращается значение типа variant, значение которого равно null. **ReadText** не может использоваться для чтения в обратном направлении.

> [!NOTE]
> Метод **ReadText** используется с потоками текст ([Тип](type-property-ado-stream.md) — **adTypeText**). Для двоичного файла потоков (**Тип** — **adTypeBinary**), используйте [чтения](read-method-ado.md).

