---
title: событие onError (RDS)
TOCTitle: onError event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc51522d143306d9625cdc07251edfe1dddf22d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288478"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="cb396-102">событие onError (RDS)</span><span class="sxs-lookup"><span data-stu-id="cb396-102">onError event (RDS)</span></span>

<span data-ttu-id="cb396-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb396-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb396-104">Событие **onError** возникает при любой ошибке во время операции.</span><span class="sxs-lookup"><span data-stu-id="cb396-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb396-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb396-105">Syntax</span></span>

<span data-ttu-id="cb396-106">onError *SCode*, *Description*, *Source*, *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="cb396-106">onError *SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="cb396-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb396-107">Parameters</span></span>

|<span data-ttu-id="cb396-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="cb396-108">Parameter</span></span>|<span data-ttu-id="cb396-109">Описание</span><span class="sxs-lookup"><span data-stu-id="cb396-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="cb396-110">*SCode*</span><span class="sxs-lookup"><span data-stu-id="cb396-110">*SCode*</span></span> |<span data-ttu-id="cb396-111">Integer that indicates the status code of the error.</span><span class="sxs-lookup"><span data-stu-id="cb396-111">An integer that indicates the status code of the error.</span></span>|
|<span data-ttu-id="cb396-112">*Описание*</span><span class="sxs-lookup"><span data-stu-id="cb396-112">*Description*</span></span> |<span data-ttu-id="cb396-113">**Строка,** которая указывает описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="cb396-113">A **String** that indicates a description of the error.</span></span>|
|<span data-ttu-id="cb396-114">*Source*</span><span class="sxs-lookup"><span data-stu-id="cb396-114">*Source*</span></span> |<span data-ttu-id="cb396-115">**Строка,** которая указывает запрос или команду, которая вызвала ошибку.</span><span class="sxs-lookup"><span data-stu-id="cb396-115">A **String** that indicates the query or command that caused the error.</span></span>|
|<span data-ttu-id="cb396-116">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="cb396-116">*CancelDisplay*</span></span> |<span data-ttu-id="cb396-117">**Boolean** value, which if set to **True,** that prevents the error from being displayed in a dialog box.</span><span class="sxs-lookup"><span data-stu-id="cb396-117">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>|

