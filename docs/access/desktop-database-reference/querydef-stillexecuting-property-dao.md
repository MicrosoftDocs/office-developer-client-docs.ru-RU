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

*выражения* . StillExecuting

*выражение*: переменная, представляющая объект **QueryDef**.

## <a name="remarks"></a>Примечания

Используйте **свойство StillExecuting,** чтобы определить, завершен ли **[](querydef-execute-method-dao.md)** последний метод асинхронного выполнения или **[OpenConnection](dbengine-openconnection-method-dao.md)** (то есть метод, выполненный с помощью параметра **dbRunAsync).** Несмотря на то, что свойство **StillExecuting** **является True,** доступ к любому возвращенного объекта невозможно получить.

После возвращения **свойства StillExecuting** **False** после вызова **OpenConnection,** **[](connection-object-dao.md)** возвращаемого связанному объекту Подключения, можно ссылаться на объект. До тех пор, пока **StillExecuting** остается **True,** объект может не ссылаться, кроме как на чтение свойства **StillExecuting.**

Чтобы завершить выполнение задачи в процессе выполнения, используйте метод **[Cancel.](connection-cancel-method-dao.md)**

