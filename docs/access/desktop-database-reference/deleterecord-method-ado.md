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

Удаляет сущность, представленную [записью.](record-object-ado.md)

## <a name="syntax"></a>Синтаксис

*Запись*.**DeleteRecord***Source*, *Async*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Source* |Необязательный параметр. **Строка,** которая содержит URL-адрес, идентифицирующий удаляемую сущность (например, файл или каталог). Если *source* опущен или указывает пустую строку, объект, [](record-object-ado.md) представленный текущей записью, удаляется. Если запись является записью коллекции ([RecordType](recordtype-property-ado.md) **adCollectionRecord,** например каталогом), все его подпапки (например, подкадиреты) также будут удалены.|
|*Async* |Необязательный параметр. **Boolean** value that, when **True,** specifies that the delete operation is asynchronous.|

## <a name="remarks"></a>Заметки

Операции с объектом, представленным этой **записью,** могут завершиться сбой после завершения этого метода. После вызова **DeleteRecord** запись должна быть закрыта, так как поведение записи может стать  непредсказуемым в зависимости от того, когда поставщик обновляет запись с помощью источника данных.  

Если эта **запись** была получена из [recordset,](recordset-object-ado.md)результаты этой операции не будут немедленно отражены в **наборе записей.** **Обновите набор записей,** закрыв и снова открыв его или выполнив методы **Recordset** [Requery](requery-method-ado.md)или [Update](update-method-ado.md) и [Resync.](resync-method-ado.md)

> [!NOTE]
> URL-адреса, использующие схему HTTP, автоматически вызывают поставщика [Microsoft OLE DB для интернет-публикации.](microsoft-ole-db-provider-for-internet-publishing.md) Дополнительные сведения см. в [сведениях об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md)


