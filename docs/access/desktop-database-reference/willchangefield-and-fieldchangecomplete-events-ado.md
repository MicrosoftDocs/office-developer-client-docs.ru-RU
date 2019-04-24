---
title: События события willchangefield и FieldChangeComplete (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fd952cc09f410752f3eb7b5963059f8d6ee7c2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302487"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a>События события willchangefield и FieldChangeComplete (ADO)

**Область применения**: Access 2013, Office 2013

Событие **события willchangefield** вызывается до того, как ожидающая операция изменяет значение одного или нескольких объектов [field](field-object-ado.md) в [наборе записей](recordset-object-ado.md). Событие **FieldChangeComplete** вызывается после того, как значение одного или нескольких объектов **поля** изменилось.

## <a name="syntax"></a>Синтаксис

События willchangefield*кфиелдс*, *Fields*, *адстатус*, пред **

FieldChangeComplete*кфиелдс*, *Fields*, *Перрор*, *адстатус*, пред **

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Кфиелдс* |Значение **типа Long** , которое указывает количество объектов **field** в *полях*.|
|*Fields* |Для **события willchangefield**параметр *Fields* представляет собой массив **Variant** , содержащий объекты **field** с исходными значениями. <br/><br/>Для **FieldChangeComplete**параметр *Fields* представляет собой массив **Variant** , содержащий объекты **field** с измененными значениями.|
|*Перрор* |Объект [Error](error-object-ado.md) . В нем описывается ошибка, которая возникла, если значение *адстатус* равно **адстатусеррорсоккурред**; в противном случае он не задается.|
|*Адстатус* |[Евентстатусенум](eventstatusenum.md). При вызове **события willchangefield** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно. Он имеет значение **адстатускантдени** , если данное событие не может запрашивать отмену ожидающей операции. <br/><br/>При вызове **FieldChangeComplete** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно, или значение **адстатусеррорсоккурред** , если операция завершилась неудачно. <br/><br/>Перед возвратом **события willchangefield** присвойте этому параметру значение **адстатусканцел** , чтобы запросить отмену ожидающей операции. <br/><br/>Перед возвратом **FieldChangeComplete** присвойте этому параметру значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений.|
|*предшнур* |Объект **Recordset** . Объект **Recordset** , для которого произошло это событие.|

## <a name="remarks"></a>Замечания

Событие **события willchangefield** или **FieldChangeComplete** может возникнуть при задании свойства [value](value-property-ado.md) и вызове метода [Update](update-method-ado.md) с параметрами массива Field и value.

