---
title: Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf01eab7-164d-c3b3-8bb0-9281e2119bc5
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: 419c9ae734e8b58d0958970e7127b94d220b8382
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345950"
---
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Открытие хранилища на удаленном сервере, если Outlook работает в режиме кэширования Exchange

**Область применения**: Outlook 2013 | Outlook 2016 
  
В этом разделе приведен пример кода на языке C++, в котором показано, как использовать флаг **мдб_онлине** для открытия хранилища сообщений на удаленном сервере, когда microsoft Outlook 2010 или microsoft Outlook 2013 находится в режиме кэширования Exchange. 
  
Режим кэширования Exchange позволяет Outlook 2010 и Outlook 2013 использовать локальную копию почтового ящика пользователя, а Outlook 2010 или Outlook 2013 поддерживает сетевое подключение к удаленной копии почтового ящика пользователя на удаленном сервере Exchange. Когда Outlook 2010 или Outlook 2013 работает в режиме кэширования Exchange, по умолчанию все решения MAPI, которые выполняют вход в тот же сеанс, также подключаются к кэшированному хранилищу сообщений. Все данные, к которым обращается доступ, и все внесенные изменения вносятся в локальную копию почтового ящика.
  
Клиент или поставщик услуг может переопределить подключение к локальному хранилищу сообщений и открыть хранилище на удаленном сервере, установив бит для **мдб_онлине** в параметре *ulFlags* при вызове [IMAPISession:: опенмсгсторе](imapisession-openmsgstore.md). После успешного открытия хранилища на удаленном сервере для этого сеанса можно использовать [IMAPISession:: OpenEntry](imapisession-openentry.md) , чтобы открыть элементы или папки в удаленном хранилище. 
  
Вы не можете открыть хранилище Exchange в режиме кэширования и в некэшированном режиме одновременно в том же сеансе MAPI. Если вы уже открыли хранилище кэшированных сообщений, потребуется его закрыть перед открытием с этим флагом или открыть новый сеанс MAPI, в котором можно будет открыть хранилище Exchange на удаленном сервере с использованием этого флага.
  
В приведенном ниже примере кода показано, как вызывать **IMAPISession:: опенмсгсторе** с флагом **мдб_онлине** , установленНым в параметре *ulFlags* , чтобы открыть хранилище по умолчанию на удаленном сервере. 
  
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
- [��������� MAPI](mapi-constants.md)
- [Доступ к хранилищу на удаленном сервере, если Outlook работает в режиме кэширования Exchange](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

