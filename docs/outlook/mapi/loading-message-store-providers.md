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
ms.openlocfilehash: fe3a76fa246cba9447db2f99562670973af183ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307807"
---
# <a name="loading-message-store-providers"></a><span data-ttu-id="e44cc-103">Загрузка поставщиков хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="e44cc-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="e44cc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e44cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e44cc-105">Когда клиентское приложение открывает хранилище сообщений, MAPI загружает в память DLL поставщика хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="e44cc-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="e44cc-106">После того как MAPI загрузит БИБЛИОТЕКУ DLL, между поставщиком хранилища сообщений и MAPI возникает очень конкретная последовательность вызовов метода.</span><span class="sxs-lookup"><span data-stu-id="e44cc-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="e44cc-107">Эта последовательность вызовов метода позволяет интерфейсу MAPI получить Функцииimsprovider верхнего уровня [: IUnknown](imsprovideriunknown.md), [имслогон: IUnknown](imslogoniunknown.md)и [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) интерфейсы и позволяет поставщику хранилища сообщений получать объект поддержки MAPI.</span><span class="sxs-lookup"><span data-stu-id="e44cc-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="e44cc-108">После выполнения последовательности вызовов поставщик хранилища сообщений должен быть готов к приему входов от клиентов.</span><span class="sxs-lookup"><span data-stu-id="e44cc-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="e44cc-109">Последовательность вызовов при загрузке библиотеки DLL поставщика сообщений выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e44cc-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="e44cc-110">Клиент вызывает [IMAPISession:: опенмсгсторе](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="e44cc-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="e44cc-111">Если хранилище сообщений еще не открыто, MAPI загружает БИБЛИОТЕКУ DLL поставщика хранилища и вызывает точку входа [МСПРОВИДЕРИНИТ](msproviderinit.md) DLL.</span><span class="sxs-lookup"><span data-stu-id="e44cc-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="e44cc-112">Если хранилище сообщений уже открыто, MAPI пропускает действия 2 и 3, а затем использует существующий интерфейс [функцииimsprovider: IUnknown](imsprovideriunknown.md) для выполнения шага 4.</span><span class="sxs-lookup"><span data-stu-id="e44cc-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="e44cc-113">**Мспровидеринит** создает и возвращает объект **функцииimsprovider** .</span><span class="sxs-lookup"><span data-stu-id="e44cc-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="e44cc-114">MAPI вызывает [функцииimsprovider:: logon](imsprovider-logon.md), передавая идентификатор записи хранилища сообщений клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="e44cc-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="e44cc-115">**Функцииimsprovider:: logon** создает и возвращает интерфейс [имслогон: IUnknown](imslogoniunknown.md) и интерфейс [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) , а затем вызывает метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) для интерфейса [имаписуппорт: IUnknown](imapisupportiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="e44cc-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="e44cc-116">Если идентификатор записи в банке сообщений клиента ссылается на уже открытое хранилище сообщений, поставщик хранилища сообщений может возвращать существующие интерфейсы **имслогон** и **IMsgStore** , а также не должен вызывать **AddRef** в своем объекте поддержки.</span><span class="sxs-lookup"><span data-stu-id="e44cc-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="e44cc-117">Если клиент не установил флаг МАПИ_НО_МАИЛ при входе в систему и не задал МДБ_НО_МАИЛ в действии 1, MAPI передает идентификатор записи в буфер обмена MAPI, чтобы диспетчер очереди MAPI мог войти в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="e44cc-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="e44cc-118">MAPI возвращает клиенту интерфейс **IMsgStore** .</span><span class="sxs-lookup"><span data-stu-id="e44cc-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="e44cc-119">Диспетчер очереди MAPI вызывает [функцииimsprovider:: спулерлогон](imsprovider-spoolerlogon.md).</span><span class="sxs-lookup"><span data-stu-id="e44cc-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="e44cc-120">**Функцииimsprovider:: спулерлогон** возвращает те же интерфейсы **имслогон** и **IMsgStore** , что и на шаге 5.</span><span class="sxs-lookup"><span data-stu-id="e44cc-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="e44cc-121">Если при входе в систему поставщика хранилища сообщений возникает ошибка, так как был введен неправильный пароль, а поставщик хранилища сообщений не может отобразить интерфейс для запроса правильного пароля, он должен возвратить МАПИ_Е_ФАИЛОНЕПРОВИДЕР из \*\*функцииimsprovider:: logon \*\*метод.</span><span class="sxs-lookup"><span data-stu-id="e44cc-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="e44cc-122">Это позволит клиентам запрашивать пароль для повторного входа в систему поставщика хранилища сообщений вместо того, чтобы запретить поставщику использовать MAPI для всего сеанса.</span><span class="sxs-lookup"><span data-stu-id="e44cc-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e44cc-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e44cc-123">See also</span></span>



[<span data-ttu-id="e44cc-124">Разработка поставщика хранилища сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="e44cc-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

