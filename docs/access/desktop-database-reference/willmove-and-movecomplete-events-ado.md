---
title: События события WillMove и MoveComplete (ADO)
TOCTitle: WillMove and MoveComplete events (ADO)
ms:assetid: fe7eb823-b388-6b3d-1ae9-056018032ef5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250307(v=office.15)
ms:contentKeyID: 48548937
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e663e18a13803097d490e0e315d139e6e15400da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306057"
---
# <a name="willmove-and-movecomplete-events-ado"></a>События события WillMove и MoveComplete (ADO)

**Область применения**: Access 2013, Office 2013

Событие **события WillMove** вызывается до того, как ожидающая операция меняет текущую позицию в [наборе записей](recordset-object-ado.md). Событие **MoveComplete** вызывается после изменения текущей позиции в **наборе записей** .

## <a name="syntax"></a>Синтаксис

События WillMove*адреасон*, *адстатус*, *pRecordset* пред

MoveComplete*адреасон*, *перрор*, *адстатус*, *pRecordset* пред

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*адреасон* |Значение [евентреасоненум](eventreasonenum.md) , указывающее причину этого события. Возможные значения: **адрснмовефирст**, **адрснмовеласт**, **адрснмовенекст**, **адрснмовепревиаус**, **адрснмове**или **адрснрекуери**.|
|*перрор* |Объект [Error](error-object-ado.md) . В нем описывается ошибка, которая возникла, если значение *адстатус* равно **адстатусеррорсоккурред**; в противном случае он не задается.|
|*адстатус* |[Евентстатусенум](eventstatusenum.md). При вызове **события WillMove** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно. Он имеет значение **адстатускантдени** , если данное событие не может запрашивать отмену ожидающей операции. <br/><br/>При вызове **MoveComplete** этот параметр имеет значение **адстатусок** , если операция, вызвавшая событие, прошла успешно, или значение **адстатусеррорсоккурред** , если операция завершилась неудачно. <br/><br/>Перед возвратом **события WillMove** присвойте этому параметру значение **адстатусканцел** , чтобы запросить отмену ожидающей операции, или присвойте этому параметру значение адстатусунвантедевент, чтобы предотвратить последующие уведомления. <br/><br/>Перед возвратом **MoveComplete** присвойте этому параметру значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений.|
|*предшнур* |Объект [Recordset](recordset-object-ado.md) . Объект **Recordset** , для которого произошло это событие.|

## <a name="remarks"></a>Примечания

События **события WillMove** или **MoveComplete** могут возникать из-за следующих операций с **набором записей** :

- [Open](open-method-ado-recordset.md)
- [Move](move-method-ado.md)
- [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveLast](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [MoveNext](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) 
- [MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)
- [AddNew](addnew-method-ado.md)
- [Requery](requery-method-ado.md)

Эти события могут возникать из-за следующих свойств:

- [Filter](filter-property-ado.md)
- [Индекс](index-property-ado.md)
- [Bookmark](bookmark-property-ado.md)
- [AbsolutePage](absolutepage-property-ado.md)
- [AbsolutePosition](absoluteposition-property-ado.md)

Эти события также возникают, если для дочернего объекта **Recordset** имеются связанные события **Recordset** и перемещен родительский **набор записей** .

Необходимо задать для параметра *адстатус* значение **адстатусунвантедевент** для каждого возможного значения *адреасон* , чтобы полностью остановить уведомление о событии для любого события, включающего параметр *адреасон* .

