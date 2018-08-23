---
title: Загрузка поставщиков хранилищ сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 632d3ef9-43c5-429a-84d7-2dce543d49fb
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 47b209b9a8818cf235b7c28593da5778dd944989
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568702"
---
# <a name="loading-message-store-providers"></a><span data-ttu-id="330a5-103">Загрузка поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="330a5-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="330a5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="330a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="330a5-105">При открытии хранилища сообщений клиентского приложения MAPI загружает библиотеку DLL поставщика хранилища сообщений в память.</span><span class="sxs-lookup"><span data-stu-id="330a5-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="330a5-106">После загрузки библиотеки DLL MAPI очень определенной последовательности вызовов методов происходит между поставщиком хранилища сообщений и MAPI.</span><span class="sxs-lookup"><span data-stu-id="330a5-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="330a5-107">Последовательность вызовов этот метод позволяет MAPI для получения верхнего уровня [IMSProvider: IUnknown](imsprovideriunknown.md), [IMSLogon: IUnknown](imslogoniunknown.md), и [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) интерфейсы и разрешает поставщика хранилища сообщений для получения объекта поддержки MAPI.</span><span class="sxs-lookup"><span data-stu-id="330a5-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="330a5-108">После завершения последовательности вызовов поставщика хранилища сообщений должен быть готов принять входов в систему от клиентов.</span><span class="sxs-lookup"><span data-stu-id="330a5-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="330a5-109">Последовательность вызовов, когда сообщение поставщика, который при загрузке библиотеки DLL выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="330a5-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="330a5-110">Клиент вызывает [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="330a5-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="330a5-111">Если хранилище сообщений еще не открыта, MAPI загружает библиотеку DLL поставщика хранилища и вызывает DLL-Библиотека [MSProviderInit](msproviderinit.md) Начальная точка.</span><span class="sxs-lookup"><span data-stu-id="330a5-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="330a5-112">Если уже открыт хранилища сообщений, MAPI пропускает шаги 2 и 3, а затем использует существующий [IMSProvider: IUnknown](imsprovideriunknown.md) интерфейс для выполнения шага 4.</span><span class="sxs-lookup"><span data-stu-id="330a5-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="330a5-113">**MSProviderInit** создает и возвращает объект **IMSProvider** .</span><span class="sxs-lookup"><span data-stu-id="330a5-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="330a5-114">MAPI вызывает [IMSProvider::Logon](imsprovider-logon.md), передав идентификатор записи хранилища сообщений клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="330a5-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="330a5-115">**IMSProvider::Logon** создает и возвращает [IMSLogon: IUnknown](imslogoniunknown.md) интерфейс и [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) интерфейс, а затем вызывается метод [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) его [IMAPISupport: IUnknown](imapisupportiunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="330a5-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="330a5-116">Если сообщение клиента, хранения идентификатор входа ссылается на хранилища сообщений, которое уже открыт, поставщика хранилища сообщений можно вернуть существующие интерфейсы **IMSLogon** и **IMsgStore** и не нужно вызвать **метод AddRef** для объекта его поддержки.</span><span class="sxs-lookup"><span data-stu-id="330a5-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="330a5-117">Если клиент не был указан флаг MAPI_NO_MAIL при его вход в систему, а не был указан MDB_NO_MAIL на шаге 1, MAPI предоставляет идентификатор записи хранилища сообщений очереди MAPI, диспетчер очереди MAPI может войти в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="330a5-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="330a5-118">MAPI возвращает интерфейс **IMsgStore** клиенту.</span><span class="sxs-lookup"><span data-stu-id="330a5-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="330a5-119">Диспетчер очереди MAPI вызывает [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span><span class="sxs-lookup"><span data-stu-id="330a5-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="330a5-120">**IMSProvider::SpoolerLogon** возвращает те же интерфейсы **IMSLogon** и **IMsgStore** из шага 5.</span><span class="sxs-lookup"><span data-stu-id="330a5-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="330a5-121">Если звонок входа в систему с сообщением хранения возникает ошибка поставщика, поскольку предоставлен неверный пароль и поставщика хранилища сообщений не удается отобразить интерфейс для запрашивающих правильный пароль, он должен возвращать MAPI_E_FAILONEPROVIDER из **IMSProvider::Logon **метод.</span><span class="sxs-lookup"><span data-stu-id="330a5-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="330a5-122">Это позволит клиентам возможности предложить пользователю пароль попробуйте войти на поставщика хранилища сообщений еще раз, а не вызывает ошибку MAPI могут быть поставщик для всего сеанса.</span><span class="sxs-lookup"><span data-stu-id="330a5-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="330a5-123">См. также</span><span class="sxs-lookup"><span data-stu-id="330a5-123">See also</span></span>



[<span data-ttu-id="330a5-124">���������� ���������� ��������� ��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="330a5-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

