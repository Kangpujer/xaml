<UserControl x:Class="TickerHD3"
             xmlns:my="clr-namespace:vMixTitleLibrary;assembly=vMixTitleLibrary"
             xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
             xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
             xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006" 
             xmlns:d="http://schemas.microsoft.com/expression/blend/2008" 
             mc:Ignorable="d" Width="1280" Height="720">
    <UserControl.Resources>
        <my:DoubleReverseConverter x:Key="DoubleReverseConverter"></my:DoubleReverseConverter>
        <Storyboard RepeatBehavior="Forever" x:Key="tickerStoryboard">
            <DoubleAnimation
                                                                    Storyboard.TargetName="AnimatedTicker"
                                                                    Storyboard.TargetProperty="(UIElement.RenderTransform).(TranslateTransform.X)"
                                                                    From="1920" To="{Binding ElementName=AnimatedTicker, Path=ActualWidth, Mode=OneWay, Converter={StaticResource DoubleReverseConverter}}" 
                                                                    AutoReverse="False" RepeatBehavior="Forever" Duration="0:2:0" />
        </Storyboard>
    </UserControl.Resources>
    <Grid Width="1280" Height="720">
        <Rectangle HorizontalAlignment="Left" Height="50.75" Margin="970.5,581,-198,0" Stroke="Black" VerticalAlignment="Top" Width="395.723" StrokeThickness="0" RenderTransformOrigin="0.5,0.5">
        	<Rectangle.Fill>
        		<LinearGradientBrush EndPoint="-1.743,0.453" StartPoint="1.211,0.431">
        			<GradientStop Color="Red" Offset="0"/>
        			<GradientStop Color="Red" Offset="1"/>
        			<GradientStop Color="#003B3824" Offset="0.747"/>
        			<GradientStop Color="#00140E0D" Offset="0.835"/>
        			<GradientStop Color="#001B1717" Offset="0.795"/>
        			<GradientStop Color="#1B503120" Offset="0.665"/>
        		</LinearGradientBrush>
        	</Rectangle.Fill>
        	<Rectangle.RenderTransform>
        		<TransformGroup>
        			<ScaleTransform/>
        			<SkewTransform AngleX="-37"/>
        			<RotateTransform/>
        			<TranslateTransform/>
        		</TransformGroup>
        	</Rectangle.RenderTransform>
        </Rectangle>
        <Rectangle HorizontalAlignment="Left" Height="44.667" Margin="-15,627.833,0,0" Stroke="Black" VerticalAlignment="Top" Width="1414" RadiusY="15.5" RadiusX="15.5" StrokeThickness="0">
        	<Rectangle.Fill>
        		<LinearGradientBrush EndPoint="0.5,1" StartPoint="0.5,0">
        			<GradientStop Color="#FF01175C" Offset="0"/>
        			<GradientStop Color="#FF00228B" Offset="1"/>
        			<GradientStop Color="#FF708CE4" Offset="0.542"/>
        		</LinearGradientBrush>
        	</Rectangle.Fill>
        </Rectangle>
        <Canvas VerticalAlignment="Bottom" Height="86" Margin="-3.5,0,8,40.5">
              <TextBlock Height="36" HorizontalAlignment="Left" x:Name="AnimatedTicker" Text="SAMPEL TICKER VMIX FULL HD  SEBAGAI CONTOH DARI KAMI MUNILUQ VIDEO SHOOTING KEPANJEN - MALANG 082 232 777 977 ### UNTUK SELEBIHNYA BISA ANDA EDIT MENURUT KEINGANAN ANDA. DENGAN DESAIN ELEGANT ANDA BISA MEMPROMOSIKAN  VIDEO SHOOTING MILIK ANDA DENGAN MEMBAWA TEMAN TEMAN DISEKITAR KITA. SEMOGA BERMANFAAT DENGAN MEMBELI PRODUCT KAMI MUNILUQ &amp; SEMOGA REZEKI BERTAMBAH LANCAR" VerticalAlignment="Center" Width="Auto" Foreground="White" FontSize="26.667" FontWeight="Bold" Canvas.Top="36" Canvas.Left="-523">
            	<TextBlock.RenderTransform>
						<TranslateTransform X="0" Y="0"/>
				</TextBlock.RenderTransform>
            </TextBlock>
        </Canvas>
        <TextBlock x:Name="textBlock" HorizontalAlignment="Left" Height="64" Margin="278,800,0,-144" TextWrapping="Wrap" Text="COLOUR" VerticalAlignment="Top" Width="396" FontFamily="/TICKER_LOGO_MUNILUQ;component/Fonts/#Segoe UI" FontSize="48" Foreground="#FFECDEC2"/>
        <Rectangle HorizontalAlignment="Left" Height="55.75" Margin="-15.137,621.5,0,0" Stroke="Black" VerticalAlignment="Top" Width="169.5" StrokeThickness="0" d:LayoutOverrides="HorizontalAlignment" RenderTransformOrigin="0.5,0.5">
        	<Rectangle.Fill>
        		<LinearGradientBrush EndPoint="0.5,1" StartPoint="0.5,0">
        			<GradientStop Color="Black" Offset="0"/>
        			<GradientStop Color="Black" Offset="1"/>
        			<GradientStop Color="#FF8B8B8B" Offset="0.546"/>
        		</LinearGradientBrush>
        	</Rectangle.Fill>
        	<Rectangle.RenderTransform>
        		<TransformGroup>
        			<ScaleTransform/>
        			<SkewTransform AngleX="20"/>
        			<RotateTransform/>
        			<TranslateTransform/>
        		</TransformGroup>
        	</Rectangle.RenderTransform>
        </Rectangle>
        <my:TextBlockDesign x:Name="DAY" HorizontalAlignment="Left" Height="29.693" VerticalAlignment="Bottom" Width="410.5" Fill="White" Text="{}{0:dddd dd/MM/yyyy}" FontSize="26" FontFamily="Arial Rounded MT Bold" RenderTransformOrigin="0.5,0.5" Margin="1365.491,0,-471,99.174" Stroke="#FF061717" ClipToBounds="True">
        	<my:TextBlockDesign.Effect>
        		<DropShadowEffect Color="#FF072DD8" Direction="256" ShadowDepth="2" BlurRadius="0"/>
        	</my:TextBlockDesign.Effect>
        	<my:TextBlockDesign.RenderTransform>
        		<TransformGroup>
        			<ScaleTransform/>
        			<SkewTransform/>
        			<RotateTransform/>
        			<TranslateTransform X="-357"/>
        		</TransformGroup>
        	</my:TextBlockDesign.RenderTransform>
        </my:TextBlockDesign>
        <my:TextBlockDesign HorizontalAlignment="Left" Margin="18,0,0,51.743" x:Name="txtClock" VerticalAlignment="Bottom" Height="35.757" Width="118.167" Text="{}{0:hh:mm}" FontSize="29" FontFamily="ContextBlackCondSSi" FontWeight="Bold" Fill="White" RenderTransformOrigin="0.5,0.5" d:LayoutOverrides="HorizontalAlignment" TextAlignment="Right" >
        	<my:TextBlockDesign.RenderTransform>
        		<TransformGroup>
        			<ScaleTransform/>
        			<SkewTransform/>
        			<RotateTransform/>
        			<TranslateTransform/>
        		</TransformGroup>
        	</my:TextBlockDesign.RenderTransform>
        </my:TextBlockDesign>
    </Grid>
</UserControl>

