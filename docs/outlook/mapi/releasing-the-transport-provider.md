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
ms.openlocfilehash: b8032b22c78ae34bce7e9ccfb0f0a14cdde07290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812116"
---
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="8b780-103">Выпуск поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="8b780-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="8b780-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8b780-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8b780-105">MAPI или диспетчер очереди MAPI завершении с помощью объекта транспорта входа:</span><span class="sxs-lookup"><span data-stu-id="8b780-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="8b780-106">MAPI или диспетчер очереди MAPI вызывает метод [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="8b780-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="8b780-107">Поставщика транспорта признает недействительным состояние объекта путем вызова метода [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) .</span><span class="sxs-lookup"><span data-stu-id="8b780-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="8b780-108">Поставщика транспорта признает недействительным объекты сообщений, которые являются Предопределенная во время вызова **TransportLogoff** зависит от флаги, которые были переданы **TransportLogoff**.</span><span class="sxs-lookup"><span data-stu-id="8b780-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="8b780-109">Поставщика транспорта вызывает метод [функции IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) объект поддержки для удаления поставщика транспорта строки в таблице состояния и удалять из внутренних таблиц любого уникальных идентификаторов (UID), которые были заданы с [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) метод.</span><span class="sxs-lookup"><span data-stu-id="8b780-109">The transport provider calls the support object's [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="8b780-110">Он уменьшает число объектов известные входа в систему, активных на этот объект поставщика.</span><span class="sxs-lookup"><span data-stu-id="8b780-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="8b780-111">Если число достигает нуля, MAPI вызывает метод [IXPProvider::Shutdown](ixpprovider-shutdown.md) и **выпуске** на объекте поставщика.</span><span class="sxs-lookup"><span data-stu-id="8b780-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="8b780-112">Если это последний объект известные поставщика, с помощью этой библиотеки DLL на этот процесс, MAPI вызывает функцию **FreeLibrary** на библиотеку DLL в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="8b780-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="8b780-113">Освободить память для объекта поддержки MAPI и возвращает объект поддержки метод **выпуска** .</span><span class="sxs-lookup"><span data-stu-id="8b780-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="8b780-114">Метод **TransportLogoff** возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="8b780-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="8b780-115">MAPI или диспетчер очереди MAPI вызывает **выпуска** для входа в систему объекта поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="8b780-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="8b780-116">Освобождается память для объекта.</span><span class="sxs-lookup"><span data-stu-id="8b780-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="8b780-117">MAPI или диспетчер очереди MAPI вызывает **FreeLibrary** DLL-Библиотеки поставщика.</span><span class="sxs-lookup"><span data-stu-id="8b780-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="8b780-118">Для надежности объекты поставщик и входа в систему должна появиться возможность обработки окончательной **версии** звонков на себя без необходимости их **TransportLogoff** или **Завершение работы** методов, вызываемых.</span><span class="sxs-lookup"><span data-stu-id="8b780-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="8b780-119">Если **выпуск** вызывается в таких случаях, поставщиками транспорта следует считать вызовы вызова **TransportLogoff** или **Завершение работы** с аргументом ноль, а затем **выпуска**.</span><span class="sxs-lookup"><span data-stu-id="8b780-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

