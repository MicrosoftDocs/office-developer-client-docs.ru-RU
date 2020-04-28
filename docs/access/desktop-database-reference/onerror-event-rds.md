---
title: событие OnError (RDS)
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
# <a name="onerror-event-rds"></a><span data-ttu-id="4f322-102">событие OnError (RDS)</span><span class="sxs-lookup"><span data-stu-id="4f322-102">onError event (RDS)</span></span>

<span data-ttu-id="4f322-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f322-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f322-104">Событие **OnError** вызывается при возникновении ошибки во время выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="4f322-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f322-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f322-105">Syntax</span></span>

<span data-ttu-id="4f322-106">OnError*SCode*, *Description*, *Source*, *canceldisplay AS*</span><span class="sxs-lookup"><span data-stu-id="4f322-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="4f322-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f322-107">Parameters</span></span>

|<span data-ttu-id="4f322-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="4f322-108">Parameter</span></span>|<span data-ttu-id="4f322-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4f322-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4f322-110">*SCode*</span><span class="sxs-lookup"><span data-stu-id="4f322-110">*SCode*</span></span> |<span data-ttu-id="4f322-111">Целое число, указывающее код состояния ошибки.</span><span class="sxs-lookup"><span data-stu-id="4f322-111">An integer that indicates the status code of the error.</span></span>|
|<span data-ttu-id="4f322-112">*Описание*</span><span class="sxs-lookup"><span data-stu-id="4f322-112">*Description*</span></span> |<span data-ttu-id="4f322-113">**Строка** , указывающая описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="4f322-113">A **String** that indicates a description of the error.</span></span>|
|<span data-ttu-id="4f322-114">*Source*</span><span class="sxs-lookup"><span data-stu-id="4f322-114">*Source*</span></span> |<span data-ttu-id="4f322-115">**Строка** , указывающая на запрос или команду, которая вызвала ошибку.</span><span class="sxs-lookup"><span data-stu-id="4f322-115">A **String** that indicates the query or command that caused the error.</span></span>|
|<span data-ttu-id="4f322-116">*Canceldisplay AS*</span><span class="sxs-lookup"><span data-stu-id="4f322-116">*CancelDisplay*</span></span> |<span data-ttu-id="4f322-117">**Логическое** значение, при котором задано значение **true**, которое предотвращает отображение ошибки в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="4f322-117">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>|

