---
title: Свойство QueryDef.StillExecuting (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 98e85d37-de50-afe1-dcca-01623546e0ad
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197953(v=office.15)
ms:contentKeyID: 48546505
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053584
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 60c0663eaa6857801555c6ce05f4256cfe4c290f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303418"
---
# <a name="querydefstillexecuting-property-dao"></a>Свойство QueryDef.StillExecuting (DAO)


**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение .* StillExecuting

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Примечания

Используйте свойство **StillExecuting,** чтобы определить, завершен ли **[](querydef-execute-method-dao.md)** последний метод асинхронного выполнения или **[OpenConnection](dbengine-openconnection-method-dao.md)** (то есть метод, выполняемый с помощью параметра **dbRunAsync).** Свойство **StillExecuting** имеет свойство **True,** но получить доступ к любому возвращенного объекта невозможно.

После того как **свойство StillExecuting** возвращает **false,** после вызова **OpenConnection,** который возвращает связанный объект **[Connection,](connection-object-dao.md)** на объект можно ссылаться. Если свойство **StillExecuting** остается **true,** ссылки на объект могут не быть, кроме чтения свойства **StillExecuting.**

Используйте метод **[Cancel,](connection-cancel-method-dao.md)** чтобы завершить выполнение задачи.

