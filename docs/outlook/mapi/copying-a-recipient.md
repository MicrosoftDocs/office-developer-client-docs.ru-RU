---
title: Копирование получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3a4fb1a3f76481bf1960c251a33911b871a8791c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419088"
---
# <a name="copying-a-recipient"></a><span data-ttu-id="c4543-103">Копирование получателя</span><span class="sxs-lookup"><span data-stu-id="c4543-103">Copying a Recipient</span></span>

  
  
<span data-ttu-id="c4543-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c4543-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c4543-105">Чтобы скопировать одного или несколько получателей из одного контейнера в другой или тот же контейнер, сначала убедитесь, что целевой контейнер является модификабельным.</span><span class="sxs-lookup"><span data-stu-id="c4543-105">To copy one or more recipients from one container into another or the same container, first check that the target container is modifiable.</span></span> <span data-ttu-id="c4543-106">Контейнеры, которые можно модификатировать, задают флаг AB_MODIFIABLE в **свойстве PR_CONTAINER_FLAGS** [(PidTagContainerFlags).](pidtagcontainerflags-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="c4543-106">Containers that are modifiable set the AB_MODIFIABLE flag in their **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="c4543-107">Чтобы скопировать одну или несколько записей в изменяемый контейнер, позвоните по методу [IABContainer::CopyEntries](iabcontainer-copyentries.md) контейнера назначения.</span><span class="sxs-lookup"><span data-stu-id="c4543-107">To copy one or more entries into a modifiable container, call the destination container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method.</span></span> <span data-ttu-id="c4543-108">Поскольку копирование записей адресных книг может отнимает много времени, **CopyEntries** принимает четыре параметра ввода: массив идентификаторов записей для копирования записей, ручку окна, индикатор прогресса и битмаску флагов.</span><span class="sxs-lookup"><span data-stu-id="c4543-108">Because copying address book entries can be time-consuming, **CopyEntries** accepts four input parameters: an array of entry identifiers for the entries to be copied, a window handle, a progress indicator, and a bitmask of flags.</span></span> 
  
<span data-ttu-id="c4543-109">Индикатор ручки окна и индикатор прогресса используются поставщиком адресной книги, чтобы показать пользователю состояние операции.</span><span class="sxs-lookup"><span data-stu-id="c4543-109">The window handle and progress indicator are used by the address book provider to show the status of the operation to the user.</span></span> <span data-ttu-id="c4543-110">Если необходимо отобразить прогресс, передай ручку окна родительскому окну индикатора прогресса в _параметре ulUIParam_ и не задай флаг AB_NO_DIALOG в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="c4543-110">If you want to display progress, pass a window handle for the parent window of the progress indicator in the  _ulUIParam_ parameter and do not set the AB_NO_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="c4543-111">Если у вас есть собственная реализация индикатора прогресса, передайте указатель реализации в _параметре lpProgress._</span><span class="sxs-lookup"><span data-stu-id="c4543-111">If you have your own implementation of a progress indicator, pass a pointer to the implementation in the  _lpProgress_ parameter.</span></span> <span data-ttu-id="c4543-112">Если нет, передай NULL.</span><span class="sxs-lookup"><span data-stu-id="c4543-112">If not, pass NULL.</span></span> <span data-ttu-id="c4543-113">Поставщик адресных книг будет использовать реализацию индикатора прогресса MAPI.</span><span class="sxs-lookup"><span data-stu-id="c4543-113">The address book provider will use the MAPI progress indicator implementation.</span></span> 
  
<span data-ttu-id="c4543-114">Битмаска флагов указывает, нужно ли отображать индикатор прогресса и как следует обрабатывать повторную проверку входа.</span><span class="sxs-lookup"><span data-stu-id="c4543-114">The bitmask of flags indicates whether or not you want to display a progress indicator and how duplicate entry checking should be handled.</span></span> <span data-ttu-id="c4543-115">Установите флаг AB_NO_DIALOG для подавления индикатора прогресса.</span><span class="sxs-lookup"><span data-stu-id="c4543-115">Set the AB_NO_DIALOG flag to suppress a progress indicator.</span></span> <span data-ttu-id="c4543-116">Установите флаг CREATE_CHECK_DUP_LOOSE, чтобы поручить поставщику адресной книги свободно проверять дубликаты или флаг CREATE_CHECK_DUP_STRICT для более строгой проверки дубликатов.</span><span class="sxs-lookup"><span data-stu-id="c4543-116">Set the CREATE_CHECK_DUP_LOOSE flag to instruct the address book provider to loosely check for duplicates or the CREATE_CHECK_DUP_STRICT flag for stricter duplicate checking.</span></span> <span data-ttu-id="c4543-117">Установите флаг CREATE_REPLACE, чтобы скопированные записи заменяли существующие записи, когда поставщик определяет, что существуют дубликаты.</span><span class="sxs-lookup"><span data-stu-id="c4543-117">Set the CREATE_REPLACE flag to have copied entries replace existing entries when the provider determines there are duplicates.</span></span> 
  
<span data-ttu-id="c4543-118">При копировании в контейнер личной адресной книги (PAB) поставщик копирует некоторые или все свойства для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="c4543-118">When copying into a personal address book (PAB) container, the provider copies some or all of the properties for each entry.</span></span> <span data-ttu-id="c4543-119">Так как MAPI не устанавливает требования к поставщикам, реализующих операции копирования контейнеров, нельзя делать предположения о количестве и типе свойств, скопированные с помощью записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="c4543-119">Because MAPI does not establish requirements for providers implementing container copy operations, you cannot make assumptions about the number and type of properties that are copied with an address book entry.</span></span>
  

