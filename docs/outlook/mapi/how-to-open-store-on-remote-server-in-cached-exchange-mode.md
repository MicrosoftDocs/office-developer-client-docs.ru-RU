---
title: Открыть хранилище на удаленном сервере, когда Outlook находится в режиме кэширования данных Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf01eab7-164d-c3b3-8bb0-9281e2119bc5
description: 'Дата последнего изменения: 25 июня 2012 года'
ms.openlocfilehash: 7c1b3d3d5eed6bc991f8e4fd702fa197d610c104
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584802"
---
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="66987-103">Открыть хранилище на удаленном сервере, когда Outlook находится в режиме кэширования данных Exchange</span><span class="sxs-lookup"><span data-stu-id="66987-103">Open a store on the remote server when Outlook is in Cached Exchange Mode</span></span>

<span data-ttu-id="66987-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66987-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66987-105">В этом разделе содержится пример кода на C++, в котором показано, как использовать флаг **MDB_ONLINE** для открытия хранилища сообщений на удаленном сервере, если Microsoft Outlook 2010 или Microsoft Outlook 2013 данных находится в режиме кэширования данных Exchange.</span><span class="sxs-lookup"><span data-stu-id="66987-105">This topic contains a code sample in C++ that shows how to use the **MDB_ONLINE** flag to open a message store on the remote server when Microsoft Outlook 2010 or Microsoft Outlook 2013 is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="66987-106">Режим кэширования данных Exchange позволяет Outlook 2010 и Outlook 2013 для использования локальной копии почтового ящика пользователя во время Outlook 2010 или Outlook 2013 поддерживает подключение к удаленной копии почтового ящика пользователя на удаленном сервере Exchange.</span><span class="sxs-lookup"><span data-stu-id="66987-106">Cached Exchange Mode permits Outlook 2010 and Outlook 2013 to use a local copy of a user's mailbox while Outlook 2010 or Outlook 2013 maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="66987-107">Если Outlook 2010 или Outlook 2013 работает в режиме кэширования данных Exchange по умолчанию всех решений MAPI, выполните вход на том же сеансе также подключены к хранилище кэшированных сообщений.</span><span class="sxs-lookup"><span data-stu-id="66987-107">When Outlook 2010 or Outlook 2013 is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="66987-108">Все данные, к которому осуществляется и все изменения, внесенные выполняются к локальной копии почтового ящика.</span><span class="sxs-lookup"><span data-stu-id="66987-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="66987-109">Клиент или служба поставщика можно переопределить подключения к хранилищу локального сообщения и откройте хранилище на удаленном сервере, установив бит для **MDB_ONLINE** с помощью параметра *ulFlags* при вызове [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span><span class="sxs-lookup"><span data-stu-id="66987-109">A client or service provider can override the connection to the local message store and open the store on the remote server by setting the bit for **MDB_ONLINE** in the  *ulFlags*  parameter when calling [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span> <span data-ttu-id="66987-110">После хранилище был успешно открыт на удаленном сервере для данного сеанса, можно использовать [IMAPISession::OpenEntry](imapisession-openentry.md) для открытия элементов или папок для удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="66987-110">After the store has been successfully opened on the remote server for that session, you can use [IMAPISession::OpenEntry](imapisession-openentry.md) to open items or folders on the remote store.</span></span> 
  
<span data-ttu-id="66987-111">Не удается открыть хранилища Exchange в режиме кэширования и в режиме без кэширования в то же время, в том же сеансе MAPI.</span><span class="sxs-lookup"><span data-stu-id="66987-111">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="66987-112">Если вы уже открыли хранилище кэшированных сообщений, потребуется его закрыть перед открытием с этим флагом или открыть новый сеанс MAPI, в котором можно будет открыть хранилище Exchange на удаленном сервере с использованием этого флага.</span><span class="sxs-lookup"><span data-stu-id="66987-112">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
  
<span data-ttu-id="66987-113">В следующем примере кода показано, как вызывать **IMAPISession::OpenMsgStore** с флагом **MDB_ONLINE** , задавать в параметре *ulFlags* , чтобы открыть хранилище по умолчанию на удаленном сервере.</span><span class="sxs-lookup"><span data-stu-id="66987-113">The following code sample shows how to call **IMAPISession::OpenMsgStore** with the **MDB_ONLINE** flag set in the  *ulFlags*  parameter to open the default store on the remote server.</span></span> 
  
```cpp
HRESULT HrRemoteMessageStore( 
    LPMAPISESSION lpMAPISession, 
    LPMDB* lppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMAPITABLE pStoresTbl = NULL; 
    SRestriction sres = {0}; 
    SPropValue spv = {0}; 
    LPSRowSet pRow = NULL; 
    LPMDB lpTempMDB = NULL; 
    enum {EID,NUM_COLS}; 
    static SizedSPropTagArray(NUM_COLS,sptCols) = {NUM_COLS, 
        PR_ENTRYID, 
    }; 
 
    //Obtain the table of all the message stores that are available 
    hRes = lpMAPISession-&gt;GetMsgStoresTable(0, &amp;pStoresTbl); 
     
    if (SUCCEEDED(hRes) &amp;&amp; pStoresTbl) 
    { 
        //Set up restrictions for the default store 
        sres.rt = RES_PROPERTY;                                  //Comparing a property 
        sres.res.resProperty.relop = RELOP_EQ;                   //Testing equality 
        sres.res.resProperty.ulPropTag = PR_DEFAULT_STORE;       //Tag to compare 
        sres.res.resProperty.lpProp = &amp;spv;                      //Prop tag and value to compare against 
     
        spv.ulPropTag = PR_DEFAULT_STORE;                        //Tag type 
        spv.Value.b   = TRUE;                                    //Tag value 
     
        //Convert the table to an array that can be stepped through 
        //Only one message store should have PR_DEFAULT_STORE set to true, so that only one will be returned 
        hRes = HrQueryAllRows( 
            pStoresTbl,                                          //Table to query 
            (LPSPropTagArray) &amp;sptCols,                          //Which columns to obtain 
            &amp;sres,                                               //Restriction to use 
            NULL,                                                //No sort order 
            0,                                                   //Max number of rows (0 means no limit) 
            &amp;pRow);                                              //Array to return 
 
        if (SUCCEEDED(hRes) &amp;&amp; pRow &amp;&amp; pRow-&gt;cRows) 
        {     
            //Open the first returned (default) message store 
            hRes = lpMAPISession-&gt;OpenMsgStore( 
                NULL,                                                //Window handle for dialogs 
                pRow-&gt;aRow[0].lpProps[EID].Value.bin.cb,             //size and... 
                (LPENTRYID)pRow-&gt;aRow[0].lpProps[EID].Value.bin.lpb, //value of entry to open 
                NULL,                                                //Use default interface (IMsgStore) to open store 
                MAPI_BEST_ACCESS | MDB_ONLINE,                       //Flags 
                &amp;lpTempMDB);                                         //Pointer to put the store in 
            if (SUCCEEDED(hRes) &amp;&amp; lppMDB) lppMDB* = lpTempMDB; 
        } 
    } 
    FreeProws(pRow); 
    if (pStoresTbl) pStoresTbl-&gt;Release(); 
 
    return hRes; 
}

```

## <a name="see-also"></a><span data-ttu-id="66987-114">См. также</span><span class="sxs-lookup"><span data-stu-id="66987-114">See also</span></span>

- [<span data-ttu-id="66987-115">Сведения о дополнениях для MAPI</span><span class="sxs-lookup"><span data-stu-id="66987-115">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="66987-116">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="66987-116">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="66987-117">Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange</span><span class="sxs-lookup"><span data-stu-id="66987-117">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

