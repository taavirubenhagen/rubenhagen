<script lang="ts">
	import { slide } from "svelte/transition";

    import { Text } from "$lib";
	import {
	BottomSheet,
        InlineButton,
        TextButton
    } from "../[components]";

    let imprintVisible = false;
</script>




<main class="relative overflow-x-hidden min-h-screen p-16 pt-32 pb-40">
    <BottomSheet imprint visible={imprintVisible} changeVisibility={() => imprintVisible = false}/>
    <div class='text-center'>
        <Text medium heading>Presentation Master 2 (Desktop Companion)</Text>
    </div>
    <div class="h-32"></div>
    <Text medium paragraph>
        1. Click the button to download the file, then open it to start the installation (A MacOS version is coming soon):
        <br/><br/><br/>
        <a download href="/presenter/Presentation Master 2.msi">
            <TextButton download onClick={() => {}}>
                Download for Windows
            </TextButton>
        </a>
        <br/><br/>
        <br/><br/>
        2. You might get antivirus warnings since I don't have the money to buy expensive security certificates
        (which are just a proof of security and don't improve it).
        If you are concerned about getting malware, just keep in mind that my contact info is public
        and I could therefore be made fully responsible for any security risks.<br/><br/>
        3. Refer to the <span class="text-blue-500 hover:text-blue-700"><InlineButton openInNew onClick={() => window.location.href = 'https://youtu.be/zjYiOR03C8M'}>video tutorial</InlineButton></span> if you don't know how to dismiss the warning.
        <span class="text-blue-500">If prompted, allow "Communication in private networks".</span> This is necessary since the communication between the devices uses WiFi.<br/><br/>
        4. Whenever you want to present, open this app as well as your PowerPoint presentation, then use the mobile app to connect the devices and control the presentation.<br/><br/>
        5. If you have any questions or concerns, feel free to contact me at t.ruebenhagen@gmail.com.<br/><br/>
    </Text>
    <div class="absolute z-50 bottom-0 w-full h-24 flex justify-center items-center">
        <div class="w-[45%] flex justify-end">
            <Text small paragraph>
                <InlineButton
                    invisible
                    onClick={() => imprintVisible = true}
                >
                    Imprint
                </InlineButton>
            </Text>
        </div>
        <div class="w-[10%] md:w-[5%] flex justify-center">
            <Text small paragraph>
                |
            </Text>
        </div>
        <div class="w-[45%] flex">
            <InlineButton invisible onClick={() => window.location.href="/presenter"}>
                Info
            </InlineButton>
        </div>
    </div>
</main>