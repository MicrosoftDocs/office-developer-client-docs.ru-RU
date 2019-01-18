---
title: Событие onReadyStateChange (RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ec2104634d9158d59d488b50d543cf0e57d9bd62
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699732"
---
# <a name="onreadystatechange-event-rds"></a><span data-ttu-id="29323-102">Событие onReadyStateChange (RDS)</span><span class="sxs-lookup"><span data-stu-id="29323-102">onReadyStateChange event (RDS)</span></span>

<span data-ttu-id="29323-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="29323-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="29323-104">Событие **onReadyStateChange** вызывается каждый раз, когда изменяется значение свойства [ReadyState](readystate-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="29323-104">The **onReadyStateChange** event is called whenever the value of the [ReadyState](readystate-property-rds.md) property changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="29323-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="29323-105">Syntax</span></span>

<span data-ttu-id="29323-106">onReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="29323-106">onReadyStateChange</span></span>

## <a name="parameters"></a><span data-ttu-id="29323-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="29323-107">Parameters</span></span>

<span data-ttu-id="29323-108">Нет.</span><span class="sxs-lookup"><span data-stu-id="29323-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="29323-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="29323-109">Remarks</span></span>

<span data-ttu-id="29323-110">Свойство **ReadyState** отражает ход выполнения [RDS. DataControl](datacontrol-object-rds.md) как асинхронно получает данные в его объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="29323-110">The **ReadyState** property reflects the progress of an [RDS.DataControl](datacontrol-object-rds.md) object as it asynchronously retrieves data into its [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="29323-111">Событие **onReadyStateChange** используется для отслеживания изменений в свойстве **ReadyState** каждый раз, когда они возникают.</span><span class="sxs-lookup"><span data-stu-id="29323-111">Use the **onReadyStateChange** event to monitor changes in the **ReadyState** property whenever they occur.</span></span> <span data-ttu-id="29323-112">Это эффективнее, чем периодически проверки значения свойства.</span><span class="sxs-lookup"><span data-stu-id="29323-112">This is more efficient than periodically checking the property's value.</span></span>

