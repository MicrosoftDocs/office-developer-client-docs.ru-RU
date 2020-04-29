---
title: Выпуск поставщика транспорта
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
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="18435-103">Выпуск поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="18435-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="18435-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18435-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18435-105">При завершении работы MAPI или диспетчера очереди MAPI с использованием объекта входа в систему:</span><span class="sxs-lookup"><span data-stu-id="18435-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="18435-106">MAPI или диспетчер очереди MAPI вызывает метод [иксплогон:: транспортлогофф](ixplogon-transportlogoff.md) поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="18435-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="18435-107">Поставщик транспорта делает недействительным объект status, вызывая метод [имаписуппорт:: макеинвалид](imapisupport-makeinvalid.md) .</span><span class="sxs-lookup"><span data-stu-id="18435-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="18435-108">Указывает, является ли поставщик транспорта недействительным объекты сообщений, которые отправляются или принимаются во время вызова **транспортлогофф** , зависит от флагов, переданных в **транспортлогофф**.</span><span class="sxs-lookup"><span data-stu-id="18435-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="18435-109">Поставщик транспорта вызывает метод [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) объекта support, чтобы удалить строку поставщика транспорта из таблицы состояний и удалить из внутренних таблиц все уникальные идентификаторы (UID), заданные с помощью метода [Имаписуппорт:: сетпровидеруид](imapisupport-setprovideruid.md) .</span><span class="sxs-lookup"><span data-stu-id="18435-109">The transport provider calls the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="18435-110">Он уменьшает количество известных объектов входа в систему, активных в данном объекте поставщика.</span><span class="sxs-lookup"><span data-stu-id="18435-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="18435-111">Если значение счетчика достигнет нуля, то MAPI вызывает метод [иксппровидер:: Shutdown](ixpprovider-shutdown.md) и **Release** для объекта provider.</span><span class="sxs-lookup"><span data-stu-id="18435-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="18435-112">Если это последний известный объект поставщика, использующий эту библиотеку DLL для этого процесса, MAPI вызывает функцию **FreeLibrary** в DLL позже.</span><span class="sxs-lookup"><span data-stu-id="18435-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="18435-113">Память для объекта поддержки MAPI освобождается, и метод **Release** объекта support возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="18435-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="18435-114">Метод **транспортлогофф** возвращает S_OK.</span><span class="sxs-lookup"><span data-stu-id="18435-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="18435-115">MAPI или диспетчер очереди MAPI вызывает **выпуск** для объекта входа поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="18435-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="18435-116">Освобождение памяти для объекта.</span><span class="sxs-lookup"><span data-stu-id="18435-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="18435-117">MAPI или диспетчер очереди MAPI вызывает **FreeLibrary** для библиотеки DLL поставщика.</span><span class="sxs-lookup"><span data-stu-id="18435-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="18435-118">Для надежности объекты входа и поставщика должны иметь возможность **обрабатывать окончательные** вызовы для себя, не выполняя вызов методов **транспортлогофф** или **Shutdown** .</span><span class="sxs-lookup"><span data-stu-id="18435-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="18435-119">Если в таких случаях вызывается метод **Release** , поставщики транспорта должны обрабатывать вызовы, как если бы **транспортлогофф** или **Shutdown** были вызваны с нулевым аргументом, за которым следует **выпуск**.</span><span class="sxs-lookup"><span data-stu-id="18435-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

