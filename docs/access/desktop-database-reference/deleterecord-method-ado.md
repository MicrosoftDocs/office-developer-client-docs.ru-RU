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

Удаляет объект, представленный [записью](record-object-ado.md).

## <a name="syntax"></a>Синтаксис

*Запись*. **DeleteRecord * * * Source*, *Async*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Source* |Необязательное. **Строковое** значение, содержащее URL-адрес, идентифицирующий объект (например, файл или каталог), который требуется удалить. Если параметр *Source* опущен или указывает пустую строку, объект, представленный текущей [записью](record-object-ado.md) , удаляется. Если запись является записью коллекции ([RecordType](recordtype-property-ado.md) из **адколлектионрекорд**, например каталога), все дочерние элементы (например, подкаталоги) также будут удалены.|
|*Асинхронного* |Необязательное. **Логическое** значение, которое при **значении true**указывает, что операция удаления является асинхронной.|

## <a name="remarks"></a>Примечания

Операции с объектом, представленным этой **записью** , могут завершиться с ошибками после завершения этого метода. После вызова **DeleteRecord** **запись** должна быть закрыта, так как поведение **записи** может стать непредсказуемым в зависимости от того, когда поставщик обновляет **запись** с источником данных.

Если эта **запись** была получена из объекта [Recordset](recordset-object-ado.md), результаты этой операции не будут немедленно отражены в **наборе записей**. Обновите **набор записей** , закрыв и повторно открыв его, либо выполнив [запрос](requery-method-ado.md)на обновление **набора записей** , а также методы [обновления](update-method-ado.md) и повторной [синхронизации](resync-method-ado.md) .

> [!NOTE]
> URL-адреса, использующие схему HTTP, автоматически будут вызывать [поставщик Microsoft OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md). Для получения дополнительных сведений см [абсолютные и относительные URL-адреса](absolute-and-relative-urls.md).


