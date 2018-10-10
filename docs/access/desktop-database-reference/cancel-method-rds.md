---
title: Cancel Method (RDS)
TOCTitle: Cancel Method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dcd37f8736b7ab4b953480cd28daeb3080abe07f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480578"
---
# <a name="cancel-method-rds"></a>Cancel Method (RDS)


**Применимо к**: Access 2013 | Office 2013

Отменяет выполнение ожидающих асинхронного вызова метода.

## <a name="syntax"></a>Синтаксис

*Служб удаленных рабочих СТОЛОВ*. *DataControl*. Отмена

## <a name="remarks"></a>Замечания

При вызове **Отменить** [ReadyState](readystate-property-rds.md) автоматически устанавливается значение **adcReadyStateLoaded**и [записей](recordset-object-ado.md) будет пустым.

