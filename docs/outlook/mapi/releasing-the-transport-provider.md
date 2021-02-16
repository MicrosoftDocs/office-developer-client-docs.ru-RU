---
title: Освобождение поставщика транспорта
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: '���� ���������� ���������: 7 ������� 2015 �.'
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328387"
---
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="ff6fa-103">Освобождение поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="ff6fa-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="ff6fa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff6fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff6fa-105">Когда MAPI или пулер MAPI завершит работу с объектом для переноса для логотипа:</span><span class="sxs-lookup"><span data-stu-id="ff6fa-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="ff6fa-106">MAPI или пулер MAPI вызывает метод [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="ff6fa-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="ff6fa-107">Поставщик транспорта аннулирует объект состояния, вызывая метод [IMAPISupport::MakeInvalid.](imapisupport-makeinvalid.md)</span><span class="sxs-lookup"><span data-stu-id="ff6fa-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="ff6fa-108">То, делает ли поставщик транспорта недопустимыми объекты сообщений, которые отправляются или получаются во время вызова **TransportLogoff,** зависит от флагов, переданных **в TransportLogoff.**</span><span class="sxs-lookup"><span data-stu-id="ff6fa-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="ff6fa-109">Поставщик транспорта вызывает метод [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) объекта поддержки, чтобы удалить строку поставщика транспорта из таблицы состояния и удалить из внутренних таблиц все уникальные идентификаторы (UID), которые были установлены с помощью метода [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md)</span><span class="sxs-lookup"><span data-stu-id="ff6fa-109">The transport provider calls the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="ff6fa-110">Он многчит количество активных известных объектов для работы с сайтом поставщика.</span><span class="sxs-lookup"><span data-stu-id="ff6fa-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="ff6fa-111">Если количество достигает нуля, MAPI вызывает метод [IXPProvider::Shutdown](ixpprovider-shutdown.md) и **Release** для объекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="ff6fa-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="ff6fa-112">Если это был последний известный объект поставщика, использующий эту DLL в этом процессе, MAPI вызывает функцию **FreeLibrary** для DLL позже.</span><span class="sxs-lookup"><span data-stu-id="ff6fa-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="ff6fa-113">Память для объекта поддержки MAPI освобождается, и возвращается метод **release** объекта поддержки.</span><span class="sxs-lookup"><span data-stu-id="ff6fa-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="ff6fa-114">Метод **TransportLogoff** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="ff6fa-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="ff6fa-115">MAPI или пулер MAPI вызывает **release** для объекта для эмблемы поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="ff6fa-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="ff6fa-116">Память для объекта отпущена.</span><span class="sxs-lookup"><span data-stu-id="ff6fa-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="ff6fa-117">MAPI или пулер MAPI вызывает **FreeLibrary** в DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="ff6fa-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="ff6fa-118">Для обеспечения надежности объекты для выхода и  поставщиков должны иметь возможность обрабатывать окончательные вызовы выпуска для себя без вызова методов **TransportLogoff** или **Shutdown.**</span><span class="sxs-lookup"><span data-stu-id="ff6fa-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="ff6fa-119">Если **в** таких случаях вызывается выпуск, поставщики транспорта должны рассматривать вызовы так, как если бы **вызовы TransportLogoff** или **Shutdown** были вызваны с аргументом "ноль", за которым следует **release**.</span><span class="sxs-lookup"><span data-stu-id="ff6fa-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

