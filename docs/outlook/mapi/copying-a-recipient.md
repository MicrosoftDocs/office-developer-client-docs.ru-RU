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
# <a name="copying-a-recipient"></a><span data-ttu-id="3c75f-103">Копирование получателя</span><span class="sxs-lookup"><span data-stu-id="3c75f-103">Copying a Recipient</span></span>

  
  
<span data-ttu-id="3c75f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c75f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c75f-105">Чтобы скопировать одного или нескольких получателей из одного контейнера в другой или один и тот же контейнер, сначала убедитесь, что целевой контейнер является изменяемым.</span><span class="sxs-lookup"><span data-stu-id="3c75f-105">To copy one or more recipients from one container into another or the same container, first check that the target container is modifiable.</span></span> <span data-ttu-id="3c75f-106">Изменяемые контейнеры устанавливают флаг АБ_МОДИФИАБЛЕ в свойстве \*\*пр_контаинер_флагс\*\* ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3c75f-106">Containers that are modifiable set the AB_MODIFIABLE flag in their **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="3c75f-107">Чтобы скопировать одну или несколько записей в изменяемый контейнер, вызовите метод [иабконтаинер:: копентриес](iabcontainer-copyentries.md) конечного контейнера.</span><span class="sxs-lookup"><span data-stu-id="3c75f-107">To copy one or more entries into a modifiable container, call the destination container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method.</span></span> <span data-ttu-id="3c75f-108">Так как копирование записей адресной книги может занимать много времени, **копентриес** принимает четыре входных параметра: массив идентификаторов записей для копируемых записей, дескриптора окна, индикатор хода выполнения и битовую маску флагов.</span><span class="sxs-lookup"><span data-stu-id="3c75f-108">Because copying address book entries can be time-consuming, **CopyEntries** accepts four input parameters: an array of entry identifiers for the entries to be copied, a window handle, a progress indicator, and a bitmask of flags.</span></span> 
  
<span data-ttu-id="3c75f-109">Дескриптор окна и индикатор хода выполнения используются поставщиком адресной книги для отображения состояния операции для пользователя.</span><span class="sxs-lookup"><span data-stu-id="3c75f-109">The window handle and progress indicator are used by the address book provider to show the status of the operation to the user.</span></span> <span data-ttu-id="3c75f-110">Если требуется отобразить ход выполнения, передайте дескриптор окна для родительского окна индикатора хода выполнения в параметре _улуипарам_ и не задавайте флаг аб_но_диалог в параметре _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="3c75f-110">If you want to display progress, pass a window handle for the parent window of the progress indicator in the  _ulUIParam_ parameter and do not set the AB_NO_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="3c75f-111">Если у вас есть собственная реализация индикатора хода выполнения, передайте указатель на реализацию в параметре _лппрогресс_ .</span><span class="sxs-lookup"><span data-stu-id="3c75f-111">If you have your own implementation of a progress indicator, pass a pointer to the implementation in the  _lpProgress_ parameter.</span></span> <span data-ttu-id="3c75f-112">В противном случае передайте значение NULL.</span><span class="sxs-lookup"><span data-stu-id="3c75f-112">If not, pass NULL.</span></span> <span data-ttu-id="3c75f-113">Поставщик адресных книг будет использовать реализацию индикатора выполнения MAPI.</span><span class="sxs-lookup"><span data-stu-id="3c75f-113">The address book provider will use the MAPI progress indicator implementation.</span></span> 
  
<span data-ttu-id="3c75f-114">Битовая маска флагов указывает, нужно ли отображать индикатор хода выполнения и как должна обрабатываться проверка записи дубликатов.</span><span class="sxs-lookup"><span data-stu-id="3c75f-114">The bitmask of flags indicates whether or not you want to display a progress indicator and how duplicate entry checking should be handled.</span></span> <span data-ttu-id="3c75f-115">Установите флаг АБ_НО_ДИАЛОГ для отключения индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="3c75f-115">Set the AB_NO_DIALOG flag to suppress a progress indicator.</span></span> <span data-ttu-id="3c75f-116">Установите флаг КРЕАТЕ_ЧЕКК_ДУП_ЛУСЕ, чтобы сообщить поставщику адресной книги о нестрогой проверке на наличие дубликатов или флаг КРЕАТЕ_ЧЕКК_ДУП_СТРИКТ для проверки более строгого дублирования.</span><span class="sxs-lookup"><span data-stu-id="3c75f-116">Set the CREATE_CHECK_DUP_LOOSE flag to instruct the address book provider to loosely check for duplicates or the CREATE_CHECK_DUP_STRICT flag for stricter duplicate checking.</span></span> <span data-ttu-id="3c75f-117">Установите для флага КРЕАТЕ_РЕПЛАЦЕ, что скопированные записи заменяют существующие записи, когда поставщик определит повторяющиеся записи.</span><span class="sxs-lookup"><span data-stu-id="3c75f-117">Set the CREATE_REPLACE flag to have copied entries replace existing entries when the provider determines there are duplicates.</span></span> 
  
<span data-ttu-id="3c75f-118">При копировании в контейнер личной адресной книги (PAB) поставщик копирует некоторые или все свойства каждой записи.</span><span class="sxs-lookup"><span data-stu-id="3c75f-118">When copying into a personal address book (PAB) container, the provider copies some or all of the properties for each entry.</span></span> <span data-ttu-id="3c75f-119">Так как MAPI не устанавливает требования для поставщиков, реализующих операции копирования контейнеров, вы не можете делать предположения о количестве и типе свойств, которые копируются с помощью записи адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3c75f-119">Because MAPI does not establish requirements for providers implementing container copy operations, you cannot make assumptions about the number and type of properties that are copied with an address book entry.</span></span>
  

