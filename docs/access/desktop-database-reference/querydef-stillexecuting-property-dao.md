---
title: QueryDef.StillExecuting Property (DAO)
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
ms.openlocfilehash: b8f3c62795b8e3be65b1f768a3c12092b516593c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481438"
---
# <a name="querydefstillexecuting-property-dao"></a>QueryDef.StillExecuting Property (DAO)


**Применимо к**: Access 2013 | Office 2013

## <a name="syntax"></a>Синтаксис

*выражение* . StillExecuting

*выражение* Переменная, которая представляет собой объект- **QueryDef** .

## <a name="remarks"></a>Замечания

Свойство **StillExecuting** определяет наиболее недавно вызванный асинхронный метод **[OpenConnection](dbengine-openconnection-method-dao.md)** (то есть, метод выполнен с помощью параметра **dbRunAsync** ) или **[выполнить](querydef-execute-method-dao.md)** завершена. Хотя свойство **StillExecuting** имеет **значение True**, любой возвращенный объект не были доступны.

Как только свойство **StillExecuting** возвращает **значение False**, следующий за вызовом **OpenConnection** , которое возвращает связанный объект **[подключения](connection-object-dao.md)** можно ссылка на объект. До тех пор, пока **StillExecuting** остается равным **True**, объект не может существовать ссылок, отличный от для чтения свойство **StillExecuting** .

Используйте метод **[Cancel](connection-cancel-method-dao.md)** для завершения выполнения задачи в процессе выполнения.

