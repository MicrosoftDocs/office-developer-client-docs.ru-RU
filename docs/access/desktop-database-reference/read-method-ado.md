---
title: Метод Read — ActiveX Data Objects (ADO)
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
# <a name="read-method-ado"></a>Read method (ADO)

**Область применения**: Access 2013, Office 2013

Считывает указанное количество ветвей из двоичного объекта [Stream.](stream-object-ado.md)

## <a name="syntax"></a>Синтаксис

*Variant*  =  *Stream*. Read (*NumBytes)*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*NumBytes* |Необязательный параметр. **Длинное** значение, которое указывает количество байтов для чтения из файла или значение [StreamReadEnum](streamreadenum.md) **adReadAll**, которое является значением по умолчанию.|

## <a name="return-value"></a>Возвращаемое значение

Метод **Read** считывает указанное количество ветвей или весь поток из объекта **Stream** и возвращает полученные данные в качестве **variant.**

## <a name="remarks"></a>Заметки

Если *число нумбайтов* превышает количество оставшихся в потоке, возвращаются только оставшиеся количество оставшихся данных.  Чтение данных не заполнено в соответствие с длиной, указанной *numBytes.* Если для чтения не осталось ни одинбайт, возвращается вариант со значением NULL. **Чтение** не может использоваться для чтения в обратном направлении.

> [!NOTE]
> *NumBytes* всегда измеряет вбайты. Для **текстовых объектов Stream** [(тип](type-property-ado-stream.md) **— adTypeText),** используйте [ReadText.](readtext-method-ado.md)


