---
title: onError Event (RDS)
TOCTitle: onError Event (RDS)
ms:assetid: e26a3f7f-0f00-919a-65ad-bf39ffb83e92
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250153(v=office.15)
ms:contentKeyID: 48548292
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fe6f6b78297008e25e15dc17e243ae982a5ccf3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482890"
---
# <a name="onerror-event-rds"></a><span data-ttu-id="18ab7-102">onError Event (RDS)</span><span class="sxs-lookup"><span data-stu-id="18ab7-102">onError Event (RDS)</span></span>


<span data-ttu-id="18ab7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="18ab7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="18ab7-104">События **onError** вызывается каждый раз, когда возникает ошибка во время выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="18ab7-104">The **onError** event is called whenever an error occurs during an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ab7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18ab7-105">Syntax</span></span>

<span data-ttu-id="18ab7-106">onError*SCode* *Описание* *источника* *CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="18ab7-106">onError*SCode*, *Description*, *Source*, *CancelDisplay*</span></span>

## <a name="parameters"></a><span data-ttu-id="18ab7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="18ab7-107">Parameters</span></span>

  - <span data-ttu-id="18ab7-108">*SCode*</span><span class="sxs-lookup"><span data-stu-id="18ab7-108">*SCode*</span></span>

  - <span data-ttu-id="18ab7-109">Целое число, указывающее код состояния ошибки.</span><span class="sxs-lookup"><span data-stu-id="18ab7-109">An integer that indicates the status code of the error.</span></span>

  - <span data-ttu-id="18ab7-110">*Описание*</span><span class="sxs-lookup"><span data-stu-id="18ab7-110">*Description*</span></span>

  - <span data-ttu-id="18ab7-111">**Строка** , указывающая описание ошибки.</span><span class="sxs-lookup"><span data-stu-id="18ab7-111">A **String** that indicates a description of the error.</span></span>

  - <span data-ttu-id="18ab7-112">*Source*</span><span class="sxs-lookup"><span data-stu-id="18ab7-112">*Source*</span></span>

  - <span data-ttu-id="18ab7-113">**Строка** , указывающая запроса или команды, вызвавшей ошибку.</span><span class="sxs-lookup"><span data-stu-id="18ab7-113">A **String** that indicates the query or command that caused the error.</span></span>

  - <span data-ttu-id="18ab7-114">*CancelDisplay*</span><span class="sxs-lookup"><span data-stu-id="18ab7-114">*CancelDisplay*</span></span>

  - <span data-ttu-id="18ab7-115">**Логическое** значение, которая, в случае присвоено **значение True**, который запрещает отображение в диалоговом окне ошибки.</span><span class="sxs-lookup"><span data-stu-id="18ab7-115">A **Boolean** value, which if set to **True**, that prevents the error from being displayed in a dialog box.</span></span>

