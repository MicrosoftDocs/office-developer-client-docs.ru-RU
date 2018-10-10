---
title: DeleteRecord Method (ADO)
TOCTitle: DeleteRecord Method (ADO)
ms:assetid: ba71187f-e580-bba8-f41b-bedfa0bc2b04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249895(v=office.15)
ms:contentKeyID: 48547370
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2d850234faf18a2bd6f3278ee4feade3aa3bb561
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479953"
---
# <a name="deleterecord-method-ado"></a>DeleteRecord Method (ADO)


**Применимо к**: Access 2013 | Office 2013



Удаляет сущности, представленной в [записи](record-object-ado.md).

## <a name="syntax"></a>Синтаксис

*Запись*. **макрокоманду УдалитьЗапись *** источника*, *Async*

## <a name="parameters"></a>Параметры

  - *Source*

  - Необязательный параметр. **Строковое** значение, содержащее URL-адрес определение сущности (например, файл или каталог) для удаления. Если *источник* указан или указывает пустая строка, удаляется сущности, представленной текущей [записи](record-object-ado.md) . Если запись является записью семейства сайтов ([типом записи](recordtype-property-ado.md) из **adCollectionRecord**, такие как каталог) также будут удалены все дочерние элементы (например, вложенные папки).

  - *Async*

  - Необязательный параметр. **Логическое** значение, которое, если **значение True**, указывает, что асинхронной операции удаления.

## <a name="remarks"></a>Замечания

Операции на объект, представленный этой **записи** могут завершиться с ошибкой после завершения этого метода. После вызова **макрокоманду УдалитьЗапись** **записи** должны быть закрыты, так как поведение **записи** могут стать непредсказуемое в зависимости от, когда поставщик обновляет **запись** с источником данных.

Если эта **запись** был получен из [набора записей](recordset-object-ado.md), затем результаты этой операции будет не будут отражены сразу же в **набора записей**. Обновление **набора записей** , закрыть и повторно открыть его или выполнив методы **записей** [запроса](requery-method-ado.md)или [обновления](update-method-ado.md) и [выполнить повторную синхронизацию](resync-method-ado.md) .


> [!NOTE]
> <P>URL-адреса, с помощью схемы http автоматически вызывает <A href="microsoft-ole-db-provider-for-internet-publishing.md">Поставщик Microsoft OLE DB для публикации Интернет</A>. Для получения дополнительных сведений см <A href="absolute-and-relative-urls.md">абсолютного и относительных URL-адресов</A>.</P>


