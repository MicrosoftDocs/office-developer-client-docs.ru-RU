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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300800"
---
# <a name="readtext-method-ado"></a>Метод ReadText (ADO)

**Область применения**: Access 2013, Office 2013

Считывая указанное количество символов из объекта [Text Stream.](stream-object-ado.md)

## <a name="syntax"></a>Синтаксис

*Строка*  =  *Stream*. ReadText (*NumChars*)

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*NumChars* |Необязательный параметр. **Длинное** значение, которое указывает количество символов для чтения из файла или значение [StreamReadEnum.](streamreadenum.md) Значение по умолчанию **— adReadAll.**|

## <a name="return-value"></a>Возвращаемое значение

Метод **ReadText** считыет указанное количество символов, всю строку или весь поток из объекта **Stream** и возвращает итоговую строку.

## <a name="remarks"></a>Заметки

Если *NumChar* больше количества символов, оставшихся в потоке, возвращаются только оставшиеся символы. Строка чтения не заполнена в соответствие с длиной, указанной *NumChar.* Если для чтения не осталось символов, возвращается вариант, значение которого null. **ReadText** нельзя использовать для чтения в обратном направлении.

> [!NOTE]
> Метод **ReadText** используется с текстовыми потоками [(тип](type-property-ado-stream.md) **adTypeText).** Для двоичных потоков (**Тип** **adTypeBinary),** используйте [чтение](read-method-ado.md).

