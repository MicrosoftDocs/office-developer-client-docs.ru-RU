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

Считывает указанное число символов из текстового объекта [потока](stream-object-ado.md) .

## <a name="syntax"></a>Синтаксис

*Строковый* = *поток*. ReadText (*нумчарс*)

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*нумчарс* |Необязательное. **Длинное** значение, задающее количество символов, считываемых из файла, или значение [стреамреаденум](streamreadenum.md) . Значение по умолчанию — **адреадалл**.|

## <a name="return-value"></a>Возвращаемое значение

Метод **ReadText** считывает указанное число символов, всю строку или весь поток из объекта **Stream** и возвращает результирующую строку.

## <a name="remarks"></a>Примечания

Если *нумчар* превышает количество символов в потоке, возвращаются только оставшиеся символы. Прочитанная строка не заполняется в соответствии с длиной, указанной в параметре *нумчар*. Если не осталось символов для чтения, возвращается Variant со значением NULL. Не удается использовать **ReadText** для чтения в обратном направлении.

> [!NOTE]
> Метод **ReadText** используется с текстовыми потоками ([Type](type-property-ado-stream.md) — **адтипетекст**). Для двоичных потоков (**Type** — **Адтипебинари**) используйте [Read](read-method-ado.md).

