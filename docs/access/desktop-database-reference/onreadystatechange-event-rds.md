---
title: onReadyStateChange событий (RDS)
TOCTitle: onReadyStateChange Event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bea7d7ae5a7fe0681af315c8569bf9b67d8bd82
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869234"
---
# <a name="onreadystatechange-event-rds"></a><span data-ttu-id="478d0-102">onReadyStateChange событий (RDS)</span><span class="sxs-lookup"><span data-stu-id="478d0-102">onReadyStateChange Event (RDS)</span></span>


<span data-ttu-id="478d0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="478d0-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="478d0-104">Событие **onReadyStateChange** вызывается каждый раз, когда изменяется значение свойства [ReadyState](readystate-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="478d0-104">The **onReadyStateChange** event is called whenever the value of the [ReadyState](readystate-property-rds.md) property changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="478d0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="478d0-105">Syntax</span></span>

<span data-ttu-id="478d0-106">onReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="478d0-106">onReadyStateChange</span></span>

## <a name="parameters"></a><span data-ttu-id="478d0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="478d0-107">Parameters</span></span>

<span data-ttu-id="478d0-108">Нет.</span><span class="sxs-lookup"><span data-stu-id="478d0-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="478d0-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="478d0-109">Remarks</span></span>

<span data-ttu-id="478d0-110">Свойство **ReadyState** отражает ход выполнения [RDS. DataControl](datacontrol-object-rds.md) как асинхронно получает данные в его объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="478d0-110">The **ReadyState** property reflects the progress of an [RDS.DataControl](datacontrol-object-rds.md) object as it asynchronously retrieves data into its [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="478d0-111">Событие **onReadyStateChange** используется для отслеживания изменений в свойстве **ReadyState** каждый раз, когда они возникают.</span><span class="sxs-lookup"><span data-stu-id="478d0-111">Use the **onReadyStateChange** event to monitor changes in the **ReadyState** property whenever they occur.</span></span> <span data-ttu-id="478d0-112">Это эффективнее, чем периодически проверки значения свойства.</span><span class="sxs-lookup"><span data-stu-id="478d0-112">This is more efficient than periodically checking the property's value.</span></span>

