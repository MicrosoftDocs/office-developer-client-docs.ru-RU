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
# <a name="cancel-method-rds"></a><span data-ttu-id="7ec5f-102">Метод Cancel (RDS)</span><span class="sxs-lookup"><span data-stu-id="7ec5f-102">Cancel method (RDS)</span></span>


<span data-ttu-id="7ec5f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ec5f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ec5f-104">Отменяет выполнение ожидающих вызовов асинхронного метода.</span><span class="sxs-lookup"><span data-stu-id="7ec5f-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec5f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ec5f-105">Syntax</span></span>

<span data-ttu-id="7ec5f-106">*RDS*.</span><span class="sxs-lookup"><span data-stu-id="7ec5f-106">*RDS*.</span></span> <span data-ttu-id="7ec5f-107">*DataControl*. Отмена</span><span class="sxs-lookup"><span data-stu-id="7ec5f-107">*DataControl*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="7ec5f-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="7ec5f-108">Remarks</span></span>

<span data-ttu-id="7ec5f-109">При **вызове отмены** [для ReadyState](readystate-property-rds.md) автоматически устанавливается **adcReadyStateLoaded,** и [набор записей](recordset-object-ado.md) будет пустым.</span><span class="sxs-lookup"><span data-stu-id="7ec5f-109">When you call **Cancel**, [ReadyState](readystate-property-rds.md) is automatically set to **adcReadyStateLoaded**, and the [Recordset](recordset-object-ado.md) will be empty.</span></span>

