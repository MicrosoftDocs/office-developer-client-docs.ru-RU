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
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Открыть хранилище на удаленном сервере, когда Outlook находится в режиме кэширования данных Exchange

**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе содержится пример кода на C++, в котором показано, как использовать флаг **MDB_ONLINE** для открытия хранилища сообщений на удаленном сервере, если Microsoft Outlook 2010 или Microsoft Outlook 2013 данных находится в режиме кэширования данных Exchange. 
  
Режим кэширования данных Exchange позволяет Outlook 2010 и Outlook 2013 для использования локальной копии почтового ящика пользователя во время Outlook 2010 или Outlook 2013 поддерживает подключение к удаленной копии почтового ящика пользователя на удаленном сервере Exchange. Если Outlook 2010 или Outlook 2013 работает в режиме кэширования данных Exchange по умолчанию всех решений MAPI, выполните вход на том же сеансе также подключены к хранилище кэшированных сообщений. Все данные, к которому осуществляется и все изменения, внесенные выполняются к локальной копии почтового ящика.
  
Клиент или служба поставщика можно переопределить подключения к хранилищу локального сообщения и откройте хранилище на удаленном сервере, установив бит для **MDB_ONLINE** с помощью параметра *ulFlags* при вызове [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). После хранилище был успешно открыт на удаленном сервере для данного сеанса, можно использовать [IMAPISession::OpenEntry](imapisession-openentry.md) для открытия элементов или папок для удаленного хранилища. 
  
Не удается открыть хранилища Exchange в режиме кэширования и в режиме без кэширования в то же время, в том же сеансе MAPI. Если вы уже открыли хранилище кэшированных сообщений, потребуется его закрыть перед открытием с этим флагом или открыть новый сеанс MAPI, в котором можно будет открыть хранилище Exchange на удаленном сервере с использованием этого флага.
  
В следующем примере кода показано, как вызывать **IMAPISession::OpenMsgStore** с флагом **MDB_ONLINE** , задавать в параметре *ulFlags* , чтобы открыть хранилище по умолчанию на удаленном сервере. 
  
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

## <a name="see-also"></a>См. также

- [Сведения о дополнениях для MAPI](about-mapi-additions.md) 
- [Константы MAPI](mapi-constants.md)
- [Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

