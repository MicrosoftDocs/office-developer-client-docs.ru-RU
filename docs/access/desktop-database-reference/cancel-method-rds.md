---
title: Метод Cancel (RDS)
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
# <a name="cancel-method-rds"></a>Метод Cancel (RDS)


**Область применения**: Access 2013, Office 2013

Отменяет выполнение ожидающего асинхронного вызова метода.

## <a name="syntax"></a>Синтаксис

*RDS*. *Элемент управления*. Отмена

## <a name="remarks"></a>Примечания

При вызове метода **Cancel**параметру [ReadyState](readystate-property-rds.md) автоматически присваивается значение **адкреадистателоадед**, а [набор записей](recordset-object-ado.md) будет пустым.

