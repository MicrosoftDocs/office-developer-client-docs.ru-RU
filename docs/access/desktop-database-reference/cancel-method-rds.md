---
title: Метод Cancel (RDS)
TOCTitle: Cancel method (RDS)
ms:assetid: 08f667c2-7a3f-c2e7-7bdf-3eb533defa33
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248827(v=office.15)
ms:contentKeyID: 48543109
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: afe7a01cf00cfc432757e7c6289d0e9eabc5bc0a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920125"
---
# <a name="cancel-method-rds"></a><span data-ttu-id="5ad65-102">Метод Cancel (RDS)</span><span class="sxs-lookup"><span data-stu-id="5ad65-102">Cancel method (RDS)</span></span>


<span data-ttu-id="5ad65-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ad65-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ad65-104">Отменяет выполнение ожидающих асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="5ad65-104">Cancels execution of a pending, asynchronous method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad65-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ad65-105">Syntax</span></span>

<span data-ttu-id="5ad65-106">*Служб удаленных рабочих СТОЛОВ*.</span><span class="sxs-lookup"><span data-stu-id="5ad65-106">*RDS*.</span></span> <span data-ttu-id="5ad65-107">*DataControl*. Отмена</span><span class="sxs-lookup"><span data-stu-id="5ad65-107">*DataControl*.Cancel</span></span>

## <a name="remarks"></a><span data-ttu-id="5ad65-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="5ad65-108">Remarks</span></span>

<span data-ttu-id="5ad65-109">При вызове **Отменить** [ReadyState](readystate-property-rds.md) автоматически устанавливается значение **adcReadyStateLoaded**и [записей](recordset-object-ado.md) будет пустым.</span><span class="sxs-lookup"><span data-stu-id="5ad65-109">When you call **Cancel**, [ReadyState](readystate-property-rds.md) is automatically set to **adcReadyStateLoaded**, and the [Recordset](recordset-object-ado.md) will be empty.</span></span>

