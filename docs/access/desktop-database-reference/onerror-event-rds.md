---
title: onError события (RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 17cbeece67ffa19666f6209a38159c9a2c6a44ea
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889947"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="ef207-102">onError события (RDS)</span><span class="sxs-lookup"><span data-stu-id="ef207-102">onError Event (RDS)</span></span>


<span data-ttu-id="ef207-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ef207-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ef207-104">События **onError** вызывается каждый раз, когда возникает ошибка во время выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ef207-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef207-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef207-105">Syntax</span></span>

<span data-ttu-id="ef207-106">onError*SCode* *Описание* *источника* *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="ef207-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="ef207-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef207-107">Parameters</span></span>

  - <span data-ttu-id="ef207-108">*SCode*</span><span class="sxs-lookup"><span data-stu-id="ef207-108">*SCode*</span></span>

  - <span data-ttu-id="ef207-109">Целое число, указывающее код состояния ошибки.</span><span class="sxs-lookup"><span data-stu-id="ef207-109">An integer that indicates the status code of the error.</span></span>

  - <span data-ttu-id="ef207-110">*Описание*</span><span class="sxs-lookup"><span data-stu-id="ef207-110">*Description*</span></span>

  - <span data-ttu-id="ef207-111">**Строка** , указывающая описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="ef207-111">A **String** that indicates a description of the error.</span></span>

  - <span data-ttu-id="ef207-112">*Source*</span><span class="sxs-lookup"><span data-stu-id="ef207-112">*Source*</span></span>

  - <span data-ttu-id="ef207-113">**Строка** , указывающая запроса или команды, вызвавшей ошибку.</span><span class="sxs-lookup"><span data-stu-id="ef207-113">A **String** that indicates the query or command that caused the error.</span></span>

  - <span data-ttu-id="ef207-114">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="ef207-114">*CancelDisplay*</span></span>

  - <span data-ttu-id="ef207-115">**Логическое** значение, которая, в случае присвоено **значение True**, который запрещает отображение в диалоговом окне ошибки.</span><span class="sxs-lookup"><span data-stu-id="ef207-115">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>

