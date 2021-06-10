---
title: Метод DeleteRecord (ADO)
TOCTitle: DeleteRecord method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d6ecd408bc2141ef9ff4bec8f6469a70e09bbe1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293996"
---
# <a name="deleterecord-method-ado"></a>Метод DeleteRecord (ADO)

**Область применения**: Access 2013, Office 2013

Удаляет объект, представленный [записью.](record-object-ado.md)

## <a name="syntax"></a>Синтаксис

*Запись*.**DeleteRecord***Source*, *Async*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Source* |Необязательный параметр. Значение **String,** содержаее URL-адрес, определяющий объект (например, файл или каталог), который будет удален. Если *Source* опущен или указывает пустую строку, объект, представленный текущей [записью,](record-object-ado.md) удаляется. Если запись — это запись коллекции [(RecordType](recordtype-property-ado.md) **adCollectionRecord**, например каталог), все дети (например, поднаправления) также будут удалены.|
|*Async* |Необязательный параметр. Значение **Boolean,** которое при **True** указывает, что операция удаления асинхронна.|

## <a name="remarks"></a>Примечания

Операции на объекте, представленного этой **записью,** могут завершиться сбой после завершения этого метода. После вызова **DeleteRecord** запись должна быть закрыта, так как поведение записи может стать  непредсказуемым в зависимости от того, когда поставщик обновляет запись с источником данных.  

Если эта **запись** была получена из [recordset,](recordset-object-ado.md)результаты этой операции не будут немедленно отражены в **Наборе записей.** **Обновите набор записей,** закрыв и открыв его повторно или исполнив методы [Requery](requery-method-ado.md) **Recordset** или [Update](update-method-ado.md) и [Resync.](resync-method-ado.md)

> [!NOTE]
> URL-адреса, использующие схему http, автоматически вызывают поставщика DB Microsoft [OLE для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md) Дополнительные сведения см. в [url-адресах Absolute и relative.](absolute-and-relative-urls.md)


