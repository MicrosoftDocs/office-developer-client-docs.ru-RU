---
title: События события willchangerecord и RecordChangeComplete (ADO)
TOCTitle: WillChangeRecord and RecordChangeComplete events (ADO)
ms:assetid: b21229b2-74e6-0798-95bf-0252f041831c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249851(v=office.15)
ms:contentKeyID: 48547162
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0113a7b22d0bba8e843ce9583e93eef848f872a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305987"
---
# <a name="willchangerecord-and-recordchangecomplete-events-ado"></a>События события willchangerecord и RecordChangeComplete (ADO)

**Область применения**: Access 2013, Office 2013

Событие **события willchangerecord** вызывается перед одной или несколькими записями (строк) в изменении [набора записей](recordset-object-ado.md) . Событие **RecordChangeComplete** вызывается после изменения одной или нескольких записей.

## <a name="syntax"></a>Синтаксис

События willchangerecord*адреасон*, *крекордс*, *адстатус*, *pRecordset* пред

RecordChangeComplete*адреасон*, *крекордс*, *перрор*, *адстатус*, *pRecordset* пред

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*адреасон* |Значение [евентреасоненум](eventreasonenum.md) , указывающее причину этого события. Возможные значения: **адрснадднев**, **адрснделете**, **адрснупдате**, **адрснундаупдате**, **адрснундоадднев**, **адрснундоделете**или **adRsnFirstChange**.|
|*крекордс* |**Длинное** значение, которое указывает количество изменяемых записей (затронутых).|
|*перрор* |Объект [Error](error-object-ado.md) . В нем описывается ошибка, которая возникла, если значение *адстатус* равно **адстатусеррорсоккурред**; в противном случае он не задается.|
|*адстатус* |[Евентстатусенум](eventstatusenum.md). При вызове **события willchangerecord** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно. Он имеет значение **адстатускантдени** , если данное событие не может запрашивать отмену ожидающей операции. <br/><br/>При вызове **RecordChangeComplete** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно, или значение **адстатусеррорсоккурред** , если операция завершилась неудачно. <br/><br/>Перед возвратом **события willchangerecord** присвойте этому параметру значение **адстатусканцел** , чтобы запросить отмену операции, вызвавшей данное событие, или присвойте этому параметру значение адстатусунвантедевент, чтобы предотвратить последующие уведомления. <br/><br/>Перед возвратом **RecordChangeComplete** присвойте этому параметру значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений.|
|*предшнур* |Объект **Recordset** . Объект **Recordset** , для которого произошло это событие.|

## <a name="remarks"></a>Примечания

Событие **события willchangerecord** или **RecordChangeComplete** может возникать для первого измененного поля в строке из-за следующих операций **с набором записей** : [Update](update-method-ado.md), [Delete](delete-method-ado-recordset.md), [CancelUpdate](cancelupdate-method-ado.md), [AddNew](addnew-method-ado.md), [UpdateBatch](updatebatch-method-ado.md)и [CancelBatch](cancelbatch-method-ado.md). Значение [CursorType](cursortype-property-ado.md) объекта **Recordset** определяет, какие операции приводят к возникновению событий.

Во время **события события willchangerecord** для свойства **Recordset** [Filter](filter-property-ado.md) набора записей задано значение **адфилтераффектедрекордс**. Вы не можете изменить это свойство при обработке события.

Необходимо задать для параметра Адстатус значение Адстатусунвантедевент для каждого возможного значения Адреасон, чтобы полностью остановить событие нотиЦиатион для любого события, включающего параметр Адреасон.

