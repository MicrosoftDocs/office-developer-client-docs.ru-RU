---
title: Метод Cancel (RDS)
TOCTitle: Cancel Method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8455496e8d426d26f56b902d9a089d236bde1a6a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868750"
---
# <a name="cancel-method-rds"></a><span data-ttu-id="2059d-102">Метод Cancel (RDS)</span><span class="sxs-lookup"><span data-stu-id="2059d-102">Cancel Method (RDS)</span></span>


<span data-ttu-id="2059d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2059d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2059d-104">Отменяет выполнение ожидающих асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="2059d-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="2059d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2059d-105">Syntax</span></span>

<span data-ttu-id="2059d-106">*Служб удаленных рабочих СТОЛОВ*.</span><span class="sxs-lookup"><span data-stu-id="2059d-106">*RDS*.</span></span> <span data-ttu-id="2059d-107">*DataControl*. Отмена</span><span class="sxs-lookup"><span data-stu-id="2059d-107">*DataControl*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="2059d-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="2059d-108">Remarks</span></span>

<span data-ttu-id="2059d-109">При вызове **Отменить** [ReadyState](readystate-property-rds.md) автоматически устанавливается значение **adcReadyStateLoaded**и [записей](recordset-object-ado.md) будет пустым.</span><span class="sxs-lookup"><span data-stu-id="2059d-109">When you call **Cancel**, [ReadyState](readystate-property-rds.md) is automatically set to **adcReadyStateLoaded**, and the [Recordset](recordset-object-ado.md) will be empty.</span></span>

