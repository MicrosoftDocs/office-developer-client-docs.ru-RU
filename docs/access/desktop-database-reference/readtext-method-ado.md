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

Читает указанное количество символов из объекта text [Stream.](stream-object-ado.md)

## <a name="syntax"></a>Синтаксис

*String*  =  *Stream*. ReadText *(NumChars)*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*NumChars* |Необязательный параметр. Длинное значение, которое указывает количество символов для чтения из файла или [значение StreamReadEnum.](streamreadenum.md)  По умолчанию значение **adReadAll**.|

## <a name="return-value"></a>Возвращаемое значение

Метод **ReadText** читает определенное количество символов, всю строку или весь поток из объекта **Stream** и возвращает результат строки.

## <a name="remarks"></a>Примечания

Если *numChar* больше количества символов, оставленных в потоке, возвращаются только оставшиеся символы. Чтение строки не соответствует длине, указанной *NumChar.* Если для чтения не осталось символов, возвращается вариант, значение которого null. **ReadText** нельзя использовать для чтения назад.

> [!NOTE]
> Метод **ReadText** используется с текстовыми потоками [(Type](type-property-ado-stream.md) **is adTypeText).** Для двоичных потоков **(Type** **is adTypeBinary),** используйте [Read](read-method-ado.md).

