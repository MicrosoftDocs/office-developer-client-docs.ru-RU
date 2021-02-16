---
title: Функция DOCMD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
localization_priority: Normal
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Выполняет обнаруженную команду.
ms.openlocfilehash: 9e5c02c9a90f3aab66c5d582c83d7d9d892f964c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413075"
---
# <a name="docmd-function"></a><span data-ttu-id="f57e1-103">Функция DOCMD</span><span class="sxs-lookup"><span data-stu-id="f57e1-103">DOCMD Function</span></span>

<span data-ttu-id="f57e1-104">Выполняет обнаруженную команду.</span><span class="sxs-lookup"><span data-stu-id="f57e1-104">Performs the identified command.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f57e1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f57e1-105">Syntax</span></span>

 <span data-ttu-id="f57e1-106">**DOCMD**( _commandID)_</span><span class="sxs-lookup"><span data-stu-id="f57e1-106">**DOCMD**( _commandID_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="f57e1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f57e1-107">Parameters</span></span>

|<span data-ttu-id="f57e1-108">**Имя**</span><span class="sxs-lookup"><span data-stu-id="f57e1-108">**Name**</span></span>|<span data-ttu-id="f57e1-109">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="f57e1-109">**Required/Optional**</span></span>|<span data-ttu-id="f57e1-110">**Тип данных**</span><span class="sxs-lookup"><span data-stu-id="f57e1-110">**Data Type**</span></span>|<span data-ttu-id="f57e1-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f57e1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f57e1-112">_commandID_</span><span class="sxs-lookup"><span data-stu-id="f57e1-112">_commandID_</span></span> <br/> |<span data-ttu-id="f57e1-113">Обязательна</span><span class="sxs-lookup"><span data-stu-id="f57e1-113">Required</span></span>  <br/> |<span data-ttu-id="f57e1-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="f57e1-114">**Number**</span></span> <br/> | <span data-ttu-id="f57e1-115">Команда для выполнения.</span><span class="sxs-lookup"><span data-stu-id="f57e1-115">The command to perform.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f57e1-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f57e1-116">Remarks</span></span>

<span data-ttu-id="f57e1-117">Список команд, поддерживаемых функцией DOCMD, см. в разделе "Команды DoCmd/DOCMD" справочника по автоматизации Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="f57e1-117">For a list of commands that are supported with the DOCMD function, see the topic "DoCmd/DOCMD commands" in the Microsoft Visio 2013 Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f57e1-118">Пример</span><span class="sxs-lookup"><span data-stu-id="f57e1-118">Example</span></span>

 `DOCMD (1312)`
  
<span data-ttu-id="f57e1-119">Приводит к **отобразить** диалоговое окно "Данные фигуры" в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="f57e1-119">Causes the **Shape Data** dialog box to appear in the user interface.</span></span> 
  

