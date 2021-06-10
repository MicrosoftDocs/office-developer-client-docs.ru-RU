---
title: Отмена метода (RDS)
TOCTitle: Cancel method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 35322ec058d31f92288fd06a4e8434a4256c2d74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296649"
---
# <a name="cancel-method-rds"></a>Отмена метода (RDS)


**Область применения**: Access 2013, Office 2013

Отменяет выполнение ожидаемого асинхронного вызова метода.

## <a name="syntax"></a>Синтаксис

*RDS*. *DataControl*. Отмена

## <a name="remarks"></a>Примечания

При **вызове Отмена,** [ReadyState](readystate-property-rds.md) автоматически замещается **adcReadyStateLoaded,** и [набор записей](recordset-object-ado.md) будет пустым.

