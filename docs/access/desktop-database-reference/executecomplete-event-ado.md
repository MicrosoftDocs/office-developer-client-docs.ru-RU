---
title: Событие ExecuteComplete (ADO)
TOCTitle: ExecuteComplete event (ADO)
ms:assetid: 47317d97-e373-32f4-9438-2dff46b8d367
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249219(v=office.15)
ms:contentKeyID: 48544589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a094968e70ace5e6cba1df184bf0ba57c2d7789
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293226"
---
# <a name="executecomplete-event-ado"></a>Событие ExecuteComplete (ADO)

**Область применения**: Access 2013, Office 2013

Событие **ExecuteComplete** вызвано после завершения выполнения команды.

## <a name="syntax"></a>Синтаксис

ExecuteComplete *RecordsAffected,* *pError,* *adStatus*, *pCommand*, *pRecordset*, *pConnection*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*RecordsAffected* |**Длинное** значение, указывающее количество записей, на которые влияет команда.|
|*pError* |Объект [Error.](error-object-ado.md) В ней описывается ошибка, которая произошла, если **значением adStatus** является **adStatusErrorsOccurred;** в противном случае он не установлен.|
|*adStatus* |[EventStatusEnum](eventstatusenum.md). Перед возвращением этого события установите для этого параметра **параметр adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.|
|*pCommand* |Выполненный [объект](command-object-ado.md) Command. Содержит объект **Command** даже при вызове **Connection.Execute** или **Recordset.Open** без явного создания **команды,** в которых объект **Command** создается внутри ADO.|
|*pRecordset* |Объект [Recordset,](recordset-object-ado.md) который является результатом выполненной команды. Этот **набор записей может** быть пустым. Никогда не следует уничтожать этот объект Recordset из этого обработера событий. Это приведет к нарушению доступа, когда ADO пытается получить доступ к объекту, который больше не существует.|
|*pConnection* |Объект [Connection.](connection-object-ado.md) Подключение, по которому была выполнена операция.|

## <a name="remarks"></a>Заметки

Событие **ExecuteComplete** может произойти из-за **подключения.** [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.** [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), **Recordset.** [Open](open-method-ado-recordset.md), **Recordset.** [Requery](requery-method-ado.md)или **Recordset.** [Методы NextRecordset.](nextrecordset-method-ado.md)

