---
title: События события willchangerecordset и RecordsetChangeComplete (ADO)
TOCTitle: WillChangeRecordset and RecordsetChangeComplete events (ADO)
ms:assetid: 2cec4cf9-a4e9-c386-5202-04e86f4cf8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249068(v=office.15)
ms:contentKeyID: 48543963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bfb304f41ada88e1b0546aaa4a54240b931017cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302823"
---
# <a name="willchangerecordset-and-recordsetchangecomplete-events-ado"></a>События события willchangerecordset и RecordsetChangeComplete (ADO)

**Область применения**: Access 2013, Office 2013

Событие **события willchangerecordset** вызывается до того, как ожидающая операция меняет объект [Recordset](recordset-object-ado.md). Событие **RecordsetChangeComplete** вызывается после изменения объекта **Recordset** .

## <a name="syntax"></a>Синтаксис

События willchangerecordset*адреасон*, *адстатус*, *pRecordset* пред

RecordsetChangeComplete*адреасон*, *перрор*, *адстатус*, *pRecordset* пред

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*адреасон* |Значение [евентреасоненум](eventreasonenum.md) , указывающее причину этого события. Возможные значения: **адрснрекуери**, **адрснресинч**, **адрснклосе**, **адрснопен**.|
|*адстатус* |[Евентстатусенум](eventstatusenum.md). При вызове **события willchangerecordset** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно. Он имеет значение **адстатускантдени** , если данное событие не может запрашивать отмену ожидающей операции. <br/><br/>При вызове **RecordsetChangeComplete** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно, **адстатусеррорсоккурред** в случае сбоя операции или **адстатусканцел** , если операция, связанная с ранее принятым событием **события willchangerecordset** , была отменена. <br/><br/>Перед возвратом **события willchangerecordset** присвойте этому параметру значение **адстатусканцел** , чтобы запросить отмену ожидающей операции, или присвойте этому параметру значение адстатусунвантедевент, чтобы предотвратить последующие уведомления. <br/><br/>Перед **события willchangerecordset** или **RecordsetChangeComplete** установите для этого параметра значение **адстатусунвантедевент** , чтобы предотвратить последующие уведомления.|
|*перрор* |Объект [Error](error-object-ado.md) . В нем описывается ошибка, которая возникла, если значение *адстатус* равно **адстатусеррорсоккурред**; в противном случае он не задается.|
|*предшнур* |Объект **Recordset** . Объект **Recordset** , для которого произошло это событие.|

## <a name="remarks"></a>Примечания

События **события willchangerecordset** или **RecordsetChangeComplete** могут возникать из-за методов [запроса](requery-method-ado.md) и [открытия](open-method-ado-recordset.md) объекта **Recordset** .

Если поставщик не поддерживает закладки, уведомление о событии **рекордсетчанже** возникает каждый раз, когда новые строки извлекаются из поставщика. Частота этого события зависит от свойства **рекордсеткачесизе** .

Необходимо задать для параметра **адстатус** значение **адстатусунвантедевент** для каждого возможного значения **адреасон** , чтобы полностью остановить уведомление о событии для любого события, включающего параметр **адреасон** .

