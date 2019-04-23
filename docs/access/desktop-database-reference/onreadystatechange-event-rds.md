---
title: событие Онреадистатечанже (RDS)
TOCTitle: onReadyStateChange event (RDS)
ms:assetid: 88102ee5-cca9-8ccb-5aca-55cda71abc4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249593(v=office.15)
ms:contentKeyID: 48546126
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ec2104634d9158d59d488b50d543cf0e57d9bd62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288492"
---
# <a name="onreadystatechange-event-rds"></a><span data-ttu-id="32a39-102">событие Онреадистатечанже (RDS)</span><span class="sxs-lookup"><span data-stu-id="32a39-102">onReadyStateChange event (RDS)</span></span>

<span data-ttu-id="32a39-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="32a39-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="32a39-104">Событие **онреадистатечанже** вызывается всякий раз, когда изменяется значение свойства [ReadyState](readystate-property-rds.md) .</span><span class="sxs-lookup"><span data-stu-id="32a39-104">The **onReadyStateChange** event is called whenever the value of the [ReadyState](readystate-property-rds.md) property changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="32a39-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32a39-105">Syntax</span></span>

<span data-ttu-id="32a39-106">Онреадистатечанже</span><span class="sxs-lookup"><span data-stu-id="32a39-106">onReadyStateChange</span></span>

## <a name="parameters"></a><span data-ttu-id="32a39-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="32a39-107">Parameters</span></span>

<span data-ttu-id="32a39-108">Нет.</span><span class="sxs-lookup"><span data-stu-id="32a39-108">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="32a39-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="32a39-109">Remarks</span></span>

<span data-ttu-id="32a39-110">Свойство **ReadyState** отражает ход выполнения [RDS. Объект управления](datacontrol-object-rds.md) данными асинхронно извлекает данные в объект [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="32a39-110">The **ReadyState** property reflects the progress of an [RDS.DataControl](datacontrol-object-rds.md) object as it asynchronously retrieves data into its [Recordset](recordset-object-ado.md) object.</span></span> <span data-ttu-id="32a39-111">Используйте событие **онреадистатечанже** для отслеживания изменений в свойстве **ReadyState** , когда они происходят.</span><span class="sxs-lookup"><span data-stu-id="32a39-111">Use the **onReadyStateChange** event to monitor changes in the **ReadyState** property whenever they occur.</span></span> <span data-ttu-id="32a39-112">Это более эффективно, чем периодическое извлечение значения свойства.</span><span class="sxs-lookup"><span data-stu-id="32a39-112">This is more efficient than periodically checking the property's value.</span></span>

