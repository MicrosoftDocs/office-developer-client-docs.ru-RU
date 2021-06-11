---
title: Загрузка поставщиков магазина сообщений
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
# <a name="loading-message-store-providers"></a><span data-ttu-id="277cb-103">Загрузка поставщиков магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="277cb-103">Loading Message Store Providers</span></span>

  
  
<span data-ttu-id="277cb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="277cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="277cb-105">При открываемом клиентском приложении хранилище сообщений MAPI загружает DLL поставщика сообщений в память.</span><span class="sxs-lookup"><span data-stu-id="277cb-105">When a client application opens a message store, MAPI loads the message store provider's DLL into memory.</span></span> <span data-ttu-id="277cb-106">После загрузки MAPI DLL между поставщиком хранения сообщений и MAPI возникает очень специфическая последовательность вызовов методов.</span><span class="sxs-lookup"><span data-stu-id="277cb-106">After MAPI loads the DLL, a very specific sequence of method calls occurs between the message store provider and MAPI.</span></span> <span data-ttu-id="277cb-107">Эта последовательность вызовов метода позволяет MAPI получать интерфейсы [IMSProvider верхнего уровня: IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md)и [IMsgStore: интерфейсы IMAPIProp](imsgstoreimapiprop.md) и позволяет поставщику магазина сообщений получить объект поддержки MAPI.</span><span class="sxs-lookup"><span data-stu-id="277cb-107">This method call sequence enables MAPI to get top-level [IMSProvider : IUnknown](imsprovideriunknown.md), [IMSLogon : IUnknown](imslogoniunknown.md), and [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interfaces, and allows the message store provider to get a MAPI support object.</span></span> <span data-ttu-id="277cb-108">После последовательности вызовов поставщик магазина сообщений должен быть готов принимать логотипы от клиентов.</span><span class="sxs-lookup"><span data-stu-id="277cb-108">After the call sequence, the message store provider should be ready to accept logons from clients.</span></span> 
  
<span data-ttu-id="277cb-109">Последовательность вызовов при загрузке DLL поставщика сообщений следующим образом:</span><span class="sxs-lookup"><span data-stu-id="277cb-109">The call sequence when a message provider DLL is loaded is as follows:</span></span>
  
1. <span data-ttu-id="277cb-110">Клиент вызывает [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="277cb-110">The client calls [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span>
    
2. <span data-ttu-id="277cb-111">Если хранилище сообщений еще не открыто, MAPI загружает DLL поставщика магазина и вызывает точку входа [MSProviderInit DLL.](msproviderinit.md)</span><span class="sxs-lookup"><span data-stu-id="277cb-111">If the message store is not already open, MAPI loads the store provider's DLL and calls the DLL's [MSProviderInit](msproviderinit.md) entry point.</span></span> <span data-ttu-id="277cb-112">Если хранилище сообщений уже открыто, MAPI пропускает шаги 2 и 3, а затем использует существующий [интерфейс IMSProvider: IUnknown](imsprovideriunknown.md) для выполнения шага 4.</span><span class="sxs-lookup"><span data-stu-id="277cb-112">If the message store is already open, MAPI skips steps 2 and 3, and then uses the existing [IMSProvider : IUnknown](imsprovideriunknown.md) interface to complete step 4.</span></span> 
    
3. <span data-ttu-id="277cb-113">**MSProviderInit** создает и возвращает **объект IMSProvider.**</span><span class="sxs-lookup"><span data-stu-id="277cb-113">**MSProviderInit** creates and returns an **IMSProvider** object.</span></span> 
    
4. <span data-ttu-id="277cb-114">MAPI вызывает [IMSProvider:::Logon,](imsprovider-logon.md)передав идентификатор входа в хранилище сообщений клиента.</span><span class="sxs-lookup"><span data-stu-id="277cb-114">MAPI calls [IMSProvider::Logon](imsprovider-logon.md), passing the client application's message store entry identifier.</span></span>
    
5. <span data-ttu-id="277cb-115">**IMSProvider::Logon** создает и возвращает [интерфейс IMSLogon : IUnknown](imslogoniunknown.md) и [интерфейс IMsgStore : IMAPIProp,](imsgstoreimapiprop.md) а затем вызывает метод [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) в [интерфейсе IMAPISupport : IUnknown.](imapisupportiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="277cb-115">**IMSProvider::Logon** creates and returns an [IMSLogon : IUnknown](imslogoniunknown.md) interface and an [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) interface, and then calls the [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) method on its [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> <span data-ttu-id="277cb-116">Если идентификатор входа в хранилище сообщений клиента ссылается на уже открытый магазин сообщений, поставщик магазина сообщений может вернуть существующие интерфейсы **IMSLogon** и **IMsgStore** и не вызывать **AddRef** на объекте поддержки.</span><span class="sxs-lookup"><span data-stu-id="277cb-116">If the client's message store entry identifier refers to a message store that is already open, the message store provider can return existing **IMSLogon** and **IMsgStore** interfaces and does not need to call **AddRef** on its support object.</span></span> 
    
6. <span data-ttu-id="277cb-117">Если клиент не установил флаг MAPI_NO_MAIL при входе в систему и не задаёт MDB_NO_MAIL на шаге 1, MAPI предоставляет идентификатор входа в хранилище сообщений в пулер MAPI, чтобы пульпер MAPI мог войти в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="277cb-117">If the client did not set the MAPI_NO_MAIL flag when it logged on and it did not set the MDB_NO_MAIL in step 1, MAPI gives the message store's entry identifier to the MAPI spooler so the MAPI spooler can log on to the message store.</span></span>
    
7. <span data-ttu-id="277cb-118">MAPI возвращает интерфейс **IMsgStore** клиенту.</span><span class="sxs-lookup"><span data-stu-id="277cb-118">MAPI returns the **IMsgStore** interface to the client.</span></span> 
    
8. <span data-ttu-id="277cb-119">Spooler MAPI вызывает [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span><span class="sxs-lookup"><span data-stu-id="277cb-119">The MAPI spooler calls [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md).</span></span>
    
9. <span data-ttu-id="277cb-120">**ИНТЕРФЕЙСЫ IMSProvider::SpoolerLogon** возвращают те же интерфейсы **IMSLogon** и **IMsgStore** с 5-го шага.</span><span class="sxs-lookup"><span data-stu-id="277cb-120">**IMSProvider::SpoolerLogon** returns the same **IMSLogon** and **IMsgStore** interfaces from step 5.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="277cb-121">Если вызов логона поставщику магазина сообщений не удается, так как был поставлен неправильный пароль, а поставщик магазина сообщений не может отображать интерфейс для запроса правильного пароля, он должен MAPI_E_FAILONEPROVIDER из метода **IMSProvider::Logon.**</span><span class="sxs-lookup"><span data-stu-id="277cb-121">If the logon call to the message store provider fails because an incorrect password was supplied and the message store provider cannot display an interface to ask for the correct password, it should return MAPI_E_FAILONEPROVIDER from the **IMSProvider::Logon** method.</span></span> <span data-ttu-id="277cb-122">Это позволит клиентам снова подсказыть пользователю пароль, чтобы попытаться войти в поставщик магазина сообщений, а не вызывать сбой MAPI для поставщика на протяжении всего сеанса.</span><span class="sxs-lookup"><span data-stu-id="277cb-122">This will allow clients to prompt the user for a password to try logging on to the message store provider again instead of causing MAPI to fail the provider for the entire session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="277cb-123">См. также</span><span class="sxs-lookup"><span data-stu-id="277cb-123">See also</span></span>



[<span data-ttu-id="277cb-124">Разработка поставщика хранилища сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="277cb-124">Developing a MAPI Message Store Provider</span></span>](developing-a-mapi-message-store-provider.md)

