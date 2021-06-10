---
title: Метод чтения — ActiveX объектов данных (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ce545b1a6b036cae9f92d7e1ab7ba7479e4e252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307674"
---
# <a name="read-method-ado"></a>Метод чтения (ADO)

**Область применения**: Access 2013, Office 2013

Считывает определенное количество bytes из двоичного объекта [Stream.](stream-object-ado.md)

## <a name="syntax"></a>Синтаксис

*Variant*  =  *Stream*. Read *(NumBytes)*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*NumBytes* |Необязательный параметр. **Длинное** значение, которое указывает количество байтов для чтения из файла или значение [StreamReadEnum](streamreadenum.md) **adReadAll**, которое является по умолчанию.|

## <a name="return-value"></a>Возвращаемое значение

Метод **Read** считывает определенное количество bytes или весь поток с объекта **Stream** и возвращает полученные данные в качестве **варианта**.

## <a name="remarks"></a>Примечания

Если *numBytes* превышает количество оставленных в потоке bytes, возвращаются только оставшиеся bytes. Считываемая информация не соответствует длине, указанной *NumBytes.* Если для чтения не осталось bytes, возвращается вариант со значением null. **Чтение** не может использоваться для чтения в обратном направлении.

> [!NOTE]
> *NumBytes всегда* измеряет bytes. Для объектов **text Stream** [(Type](type-property-ado-stream.md) is **adTypeText),** используйте [ReadText](readtext-method-ado.md).


