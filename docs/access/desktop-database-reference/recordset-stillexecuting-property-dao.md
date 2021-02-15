---
title: Свойство Recordset.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0e53c98f-17ac-3569-d780-540a6932013e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845245(v=office.15)
ms:contentKeyID: 48543245
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1195a45c3846cf79a45c16cda8e23bc95ef8156d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307569"
---
# <a name="recordsetstillexecuting-property-dao"></a>Свойство Recordset.StillExecuting (DAO)

**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение .* StillExecuting

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Используйте свойство **StillExecuting,** чтобы определить, завершен ли  последний метод асинхронного выполнения или **OpenConnection** (то есть метод, выполняемый с помощью параметра **dbRunAsync).** Свойство **StillExecuting** имеет свойство **True,** но получить доступ к любому возвращенного объекта невозможно.

После того как **свойство StillExecuting** возвращает **false,** после вызова **OpenConnection,** который возвращает связанный объект **Connection,** на объект можно ссылаться. Если свойство **StillExecuting** остается **true,** ссылки на объект могут не быть, кроме чтения свойства **StillExecuting.**

Используйте метод **[Cancel,](connection-cancel-method-dao.md)** чтобы завершить выполнение задачи.

