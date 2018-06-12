---
title: Копирование получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b9a41f44-4c7e-4c57-b536-63fb85e4fae6
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: dd68bc2054136a7f587b05dc56dbeabd06de1f08
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808213"
---
# <a name="copying-a-recipient"></a><span data-ttu-id="d9a87-103">Копирование получателя</span><span class="sxs-lookup"><span data-stu-id="d9a87-103">Copying a Recipient</span></span>

  
  
<span data-ttu-id="d9a87-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d9a87-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d9a87-105">Копирование одного или нескольких получателей из одного контейнера в другой или же контейнера, сначала убедитесь, что целевой контейнер можно изменить.</span><span class="sxs-lookup"><span data-stu-id="d9a87-105">To copy one or more recipients from one container into another or the same container, first check that the target container is modifiable.</span></span> <span data-ttu-id="d9a87-106">Контейнеры, которые могут быть изменены установить флаг AB_MODIFIABLE в своем свойстве **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d9a87-106">Containers that are modifiable set the AB_MODIFIABLE flag in their **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="d9a87-107">Чтобы скопировать один или несколько записей в контейнер можно изменить, вызовите метод [IABContainer::CopyEntries](iabcontainer-copyentries.md) конечного контейнера.</span><span class="sxs-lookup"><span data-stu-id="d9a87-107">To copy one or more entries into a modifiable container, call the destination container's [IABContainer::CopyEntries](iabcontainer-copyentries.md) method.</span></span> <span data-ttu-id="d9a87-108">Так как копирование адресной книги может занять много времени, **CopyEntries** принимает четыре входных параметра: массив идентификаторов запись для записи, чтобы скопировать, дескриптор окна, индикатор хода выполнения и битовую маску флагов.</span><span class="sxs-lookup"><span data-stu-id="d9a87-108">Because copying address book entries can be time-consuming, **CopyEntries** accepts four input parameters: an array of entry identifiers for the entries to be copied, a window handle, a progress indicator, and a bitmask of flags.</span></span> 
  
<span data-ttu-id="d9a87-109">Индикатор окна дескриптора и хода выполнения используются поставщик адресной книги для отображения состояния операции для пользователя.</span><span class="sxs-lookup"><span data-stu-id="d9a87-109">The window handle and progress indicator are used by the address book provider to show the status of the operation to the user.</span></span> <span data-ttu-id="d9a87-110">Если необходимо отображать ход выполнения, передайте дескриптор окна для родительского окна индикатор хода выполнения с помощью параметра _ulUIParam_ и не задан флаг AB_NO_DIALOG с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="d9a87-110">If you want to display progress, pass a window handle for the parent window of the progress indicator in the  _ulUIParam_ parameter and do not set the AB_NO_DIALOG flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="d9a87-111">При наличии внедрения индикатор хода выполнения, передайте указатель для реализации в параметре _lpProgress_ .</span><span class="sxs-lookup"><span data-stu-id="d9a87-111">If you have your own implementation of a progress indicator, pass a pointer to the implementation in the  _lpProgress_ parameter.</span></span> <span data-ttu-id="d9a87-112">В противном случае передать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="d9a87-112">If not, pass NULL.</span></span> <span data-ttu-id="d9a87-113">Поставщик адресной книги использует реализацию, индикатор хода выполнения MAPI.</span><span class="sxs-lookup"><span data-stu-id="d9a87-113">The address book provider will use the MAPI progress indicator implementation.</span></span> 
  
<span data-ttu-id="d9a87-114">Указывает битовую маску флагов ли необходимо отобразить индикатор выполнения и проверки необходимо обрабатывать как повторяющиеся записи.</span><span class="sxs-lookup"><span data-stu-id="d9a87-114">The bitmask of flags indicates whether or not you want to display a progress indicator and how duplicate entry checking should be handled.</span></span> <span data-ttu-id="d9a87-115">Установите флаг AB_NO_DIALOG, чтобы не отображать индикатор хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="d9a87-115">Set the AB_NO_DIALOG flag to suppress a progress indicator.</span></span> <span data-ttu-id="d9a87-116">Значение флага CREATE_CHECK_DUP_LOOSE для указания поставщик адресной книги на слабо наличие дубликатов или флаг CREATE_CHECK_DUP_STRICT для более строгие повторной проверки.</span><span class="sxs-lookup"><span data-stu-id="d9a87-116">Set the CREATE_CHECK_DUP_LOOSE flag to instruct the address book provider to loosely check for duplicates or the CREATE_CHECK_DUP_STRICT flag for stricter duplicate checking.</span></span> <span data-ttu-id="d9a87-117">Набор флаг CREATE_REPLACE для копирования записей заменить существующие записи при поставщик определяет, что существуют повторяющиеся значения.</span><span class="sxs-lookup"><span data-stu-id="d9a87-117">Set the CREATE_REPLACE flag to have copied entries replace existing entries when the provider determines there are duplicates.</span></span> 
  
<span data-ttu-id="d9a87-118">При копировании в адресной книге пользователя контейнер, поставщик копирует некоторые или все свойства для каждой записи.</span><span class="sxs-lookup"><span data-stu-id="d9a87-118">When copying into a personal address book (PAB) container, the provider copies some or all of the properties for each entry.</span></span> <span data-ttu-id="d9a87-119">Так как MAPI не установить требования для реализации операций копирования контейнер поставщиков, не может делать предположения относительно числа и типа свойств, которые копируются с записью адресной книги.</span><span class="sxs-lookup"><span data-stu-id="d9a87-119">Because MAPI does not establish requirements for providers implementing container copy operations, you cannot make assumptions about the number and type of properties that are copied with an address book entry.</span></span>
  

