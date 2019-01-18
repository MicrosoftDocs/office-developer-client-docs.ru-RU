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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704520"
---
# <a name="deleterecord-method-ado"></a>Метод DeleteRecord (ADO)

**Применимо к**: Access 2013, Office 2013

Удаляет сущности, представленной в [записи](record-object-ado.md).

## <a name="syntax"></a>Синтаксис

*Запись*. **макрокоманду УдалитьЗапись *** источника*, *Async*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Source* |Необязательно. **Строковое** значение, содержащее URL-адрес определение сущности (например, файл или каталог) для удаления. Если *источник* указан или указывает пустая строка, удаляется сущности, представленной текущей [записи](record-object-ado.md) . Если запись является записью семейства сайтов ([типом записи](recordtype-property-ado.md) из **adCollectionRecord**, такие как каталог) также будут удалены все дочерние элементы (например, вложенные папки).|
|*Async* |Необязательно. **Логическое** значение, которое, если **значение True**, указывает, что асинхронной операции удаления.|

## <a name="remarks"></a>Замечания

Операции на объект, представленный этой **записи** могут завершиться с ошибкой после завершения этого метода. После вызова **макрокоманду УдалитьЗапись** **записи** должны быть закрыты, так как поведение **записи** могут стать непредсказуемое в зависимости от, когда поставщик обновляет **запись** с источником данных.

Если эта **запись** был получен из [набора записей](recordset-object-ado.md), затем результаты этой операции будет не будут отражены сразу же в **набора записей**. Обновление **набора записей** , закрыть и повторно открыть его или выполнив методы **записей** [запроса](requery-method-ado.md)или [обновления](update-method-ado.md) и [выполнить повторную синхронизацию](resync-method-ado.md) .

> [!NOTE]
> URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md). Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).


